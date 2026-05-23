---
title: "Scaling LLM Inference: Innovations in Tensor Parallelism, Context Parallelism, and Expert Parallelism"
vendor: meta
source_url: https://engineering.fb.com/2025/10/17/ai-research/scaling-llm-inference-innovations-tensor-parallelism-context-parallelism-expert-parallelism/
published_at: 2025-10-17T16:00:50.000Z
crawled_at: 2026-05-23T16:30:22.000Z
word_count: 880
reading_time_minutes: 5
tags: [LLM-inference, parallelism, Meta, engineering, scaling]
---

October 17, 2025

# Scaling LLM Inference: Innovations in Tensor Parallelism, Context Parallelism, and Expert Parallelism

At Meta, we are constantly pushing the boundaries of LLM inference systems to power applications such as the Meta AI App. We are sharing how we developed and implemented advanced parallelism techniques to optimize key performance metrics related to resource efficiency, throughput, and latency.

The rapid evolution of large language models (LLMs) has ushered in a new era of AI-powered applications, from conversational agents to advanced content generation. However, deploying these massive models at scale for real-time inference presents significant challenges, particularly in achieving high throughput, low latency, and better resource efficiency.

Our primary goal is to optimize key performance metrics: Resource efficiency (maximizing GPU utilization to improve operational efficiency), Throughput (serving more users by processing a higher volume of requests), and Latency (minimizing response times for a seamless user experience). This includes Time-to-first-token (TTFT) for prefill, ideally under 350ms, and Time-to-incremental-token (TTIT) for decoding, targeting less than 25ms.

These metrics highlight the distinct computational demands of LLM inference: Prefill is compute-intensive, while decoding is memory bandwidth-intensive. To address these challenges and enable the deployment of large models, we have developed and implemented advanced parallelism techniques.

## The Two Stages of LLM Inference

A typical LLM generative-inference task unfolds in two stages. The **prefill stage** processes the input prompt (which can be thousands of tokens long) to generate a key-value (KV) cache for each transformer layer of the LLM. Prefill is **compute-bound** because the attention mechanism scales quadratically with sequence length. The **decoding stage** utilizes and incrementally updates the KV cache to generate tokens one by one. Decoding is **memory-bound**, as the I/O time of reading memory dominates attention time, with model weights and the KV cache occupying the majority of memory.

## Addressing Bottlenecks With Parallelism

To scale LLM inference effectively, especially for handling long contexts and massive models, we employ three main types of inference parallelism.

### Tensor Parallelism (TP)

Tensor parallelism improves fitting large models across multiple GPUs and achieving high throughput that a single device cannot provide. It involves sharding individual layers of the model, such as attention blocks and MLP layers, into smaller, independent blocks that can be executed on different devices.

A key challenge in tensor parallelism is the "allreduce" communication operation, which can contribute up to 30% of end-to-end latency. To mitigate this, we developed **direct data access (DDA)** algorithms:

- **DDA flat algorithm:** Improves small message-size allreduce latency by allowing each rank to directly load memory from other ranks and perform local reduce operations. This reduces latency from O(N) to O(1) by increasing the amount of data exchange from O(n) to O(n^2).
- **DDA tree algorithm:** Breaks the allreduce into two phases (reduce-scatter and all-gather) and uses direct data access in each step. This moves the same amount of data as the ring algorithm but reduces latency to a constant factor.

Our DDA solutions demonstrate significant speedups against baselines such as NCCL (NVIDIA) and RCCL (AMD ROCm). With AMD MI300X, we achieved overall performance parity with NVIDIA H100, with DDA outperforming RCCL baseline by 10-50% for decode and yielding 10-30% speedup for prefill, resulting in approximately 10% reduction in TTIT.

### Context Parallelism (CP)

Context parallelism facilitates managing and processing extremely long contexts, such as the 1M/10M token capabilities introduced with Llama 4. Long-context inference presents unique challenges: compute (dense attention FLOPs scale quadratically with context length), memory (the KV cache grows linearly with context), and communication (latency increases when parallelizing across multiple hosts).

We implemented two variants of context parallelism in the attention module, often referred to as "ring attention":

- **Pass-KV:** Input tokens are split across multiple CP ranks. Each rank calculates its portion of query, key, and value tensors. Then, key and value tensors are exchanged between ranks to enable attention interactions across the full context.
- **Pass-Q:** Similar to Pass-KV, but query tensors are exchanged between ranks.

Our optimizations enabled remarkable performance: less than one minute for one million tokens on a single H100 host and less than one minute for 10 million tokens using distributed inference across 32 H100 hosts. With Llama 3 405B, we demonstrated near-linear scaling, achieving 128K token prefill in 3.8 seconds with CP over 16 nodes, and 1M-token prefill in 77 seconds.

### Expert Parallelism (EP)

Expert parallelism helps with scaling mixture-of-experts (MoE) models, where a large number of "experts" (neural network modules) make it impossible to fit the entire model onto a single host. In EP-based inference, we utilize a two-shot, all-to-all communication pattern to exchange tokens between data parallelism and expert parallelism ranks based on routing.

The all-to-all communication can contribute 10-30% to end-to-end latency, especially for decode messages (100KB to 2MB). To optimize this, we are exploring solutions including dynamic all-to-all (sending sub-chunks of data to remote neighbors) and persistent all-to-all (addressing slowdowns caused by memory-handle exchange, network-load balancing, and CPU overhead).

## Looking Ahead: Disaggregated Inference and Future Challenges

To further optimize LLM inference, we are moving towards **N-D parallelism** (CP, PP, EP, TP across nodes, with separate DP) and **disaggregating prefill and decoding tiers**. This allows for better resource balancing and the potential to use heterogeneous hardware, where compute-heavy hardware is used for prefill and memory bandwidth-heavy hardware for decoding.

Future challenges include optimizing cloud fabric design for LLM workloads, integrating communication operations directly into computational kernels (fused kernels), and enabling devices to initiate operations directly (device-initiated kernels) to reduce CPU overhead. These advancements in parallelization and system-level improvements have helped enable the next generation of AI applications and push the boundaries of what LLMs can achieve.
