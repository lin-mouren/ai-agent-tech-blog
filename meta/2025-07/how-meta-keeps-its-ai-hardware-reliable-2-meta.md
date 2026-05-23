---
title: "How Meta keeps its AI hardware reliable"
vendor: meta
source_url: https://engineering.fb.com/2025/07/22/data-infrastructure/how-meta-keeps-its-ai-hardware-reliable/
published_at: 2025-07-22T18:45:16.000Z
crawled_at: 2026-05-23T14:18:59.000Z
word_count: 2750
reading_time_minutes: 14
tags: [ai-hardware, reliability, training, inference, sdc]
---

How Meta keeps its AI hardware reliable - Engineering at Meta

July 22, 2025

By Harish Dattatraya Dixit, Sriram Sankar

- Hardware faults can have a significant impact on AI training and inference.
- Silent data corruptions (SDCs), undetected data errors caused by hardware, can be particularly harmful for AI systems that rely on accurate data for training as well as providing useful outputs.
- We are sharing methodologies we deploy at various scales for detecting SDC across our AI and non-AI infrastructure to help ensure the reliability of AI training and inference workloads across Meta.

Meta's global AI infrastructure consists of a large number of hardware components and servers, connected via network fabric across globally distributed data centers. This infrastructure supports training large-scale models as well as advanced AI applications such as text-to-image generation and object segmentation.

Since 2018, Meta's hardware reliability journey has led to novel findings, identifying unique failure types in disks, CPUs, memories, switches, GPUs, ASICs, and networks, often leading the industry in discovering failure modes. From our experience running the Llama 3 herd of models, we find that hardware failures in components such as SRAMs, HBMs, processing grids, and network switch hardware significantly impact AI cluster reliability, with over 66% of training interruptions due to such failures.

## Types of hardware faults encountered at Meta

The hardware faults or errors that we observe in our infrastructure can be classified broadly into three categories:

### Static errors
Hardware failures often appear as binary states: A device either powers on or powers off. These static errors are straightforward to identify in large-scale fleets.

### Transient errors
Transient errors, categorized by their reproducibility, include load-dependent or partially observable faults, such as device issues from thermal runaway or random crashes from uncorrectable errors.

### Silent errors
Silent errors or silent data corruptions (SDCs) occur when hardware miscomputes without leaving detectable traces, leading applications to consume incorrect results. These errors, often due to silicon defects, can remain unnoticed for long periods unless significant deviations are observed. With increased silicon density in accelerators, silent data corruptions now occur at about one fault per thousand devices.

## Novel SDC detection mechanisms

To protect applications from silent data corruption, Meta employs several detection mechanisms:

1. **Fleetscanner:** Captures performance outliers at scale with targeted micro-benchmarks for identifying hardware defects. Tests are scheduled periodically, covering the entire fleet every 45 to 60 days.

2. **Ripple:** Co-locates with workloads, executing tests in milliseconds to seconds, allowing fleet-wide coverage in days. It overlaps test instructions across cores and threads, providing faster detection than Fleetscanner.

3. **Hardware Sentinel:** A novel, test-and-architecture-agnostic approach that evaluates application exceptions in kernel space. It identifies core-based anomalies as silent data corruption without requiring test allocations. Hardware Sentinel outperforms testing-based methods by 41% across architectures, applications, and data centers.

## Silent errors in AI hardware

AI applications such as training and inference have unique and more challenging implications for SDCs.

### SDCs in training workloads
SDCs in training workloads lead to incorrect computations, affecting both forward and backward passes. The two most common cases are NaN propagation and corrupted gradient variance.

**Not-a-Number (NaN) propagation** occurs when an SDC pushes a representable value into an incorrect representation, generating a NaN during training computations. Once a NaN is created, it propagates through subsequent computations, affecting the training iteration, accelerator domain, host domain, and eventually the entire cluster.

**Corrupted gradient variance** occurs when an SDC affects gradient calculations, leading to gradient explosion, implosion, or local minima. This corruption, while within numeric bounds, is mistakenly treated as correct, affecting the entire cluster in synchronous training.

### SDCs in inference workloads
In inference applications, SDCs lead to incorrect results, which, due to the scale of operations, affect thousands of inference consumers. Persistent SDCs can directly impact decisions made by systems such as recommendation engines or LLM outputs.

## Detection of SDCs in AI hardware

Mitigation strategies include infrastructure strategies (reductive triage, deterministic training, hyper-checkpointing) and stack strategies (gradient clipping, algorithmic fault tolerance, tri-variate computational training architecture, parameter vulnerability factors, and divergence detection).

## The Meta Training and Inference Accelerator

Meta is on an ambitious journey toward enabling training and inference accelerators under the Meta Training and Inference Accelerator (MTIA) family. Using the factory-to-fleet approach and consistently revisiting our reliability solutions across the stack, our goal is to deliver a best-in-class, reliable-and-performant solution for AI infrastructure.

Hardware faults significantly impact AI training and inference production. As cluster sizes and semiconductor complexity grow, fault complexity will exponentially increase. Solutions must involve factory-to-fleet coordination and stack-level resiliency. For AI applications, treating reliability as a primary design consideration is essential.