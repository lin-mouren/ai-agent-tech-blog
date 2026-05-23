---
title: "The Building Blocks of Agentic AI: From Kernels to Clusters"
vendor: meta
source_url: https://ai.meta.com/blog/introducing-pytorch-native-agentic-stack/
published_at: 2025-10-24T00:00:00.000Z
crawled_at: 2026-05-23T14:44:14.000Z
word_count: 1500
reading_time_minutes: 8
tags: [PyTorch, agentic-AI, open-source, Meta, reinforcement-learning]
---

October 24, 2025

# The Building Blocks of Agentic AI: From Kernels to Clusters

## Takeaways

- At PyTorch Conference 2025 in San Francisco, we unveiled five new projects spanning kernel languages, distributed systems, reinforcement learning, agentic frameworks, and edge AI deployment.
- This stack is PyTorch-native, interoperates with the vast ecosystem, and scales from thousands to hundreds of thousands of GPUs.
- We're partnering with Hugging Face to launch OpenEnv, an open reinforcement learning environment hub.

As AI moves from research into production, developers face a growing gap between cutting-edge techniques and the tools needed to build and scale them. At PyTorch Conference 2025, we introduced: ExecuTorch 1.0, Torchforge, Monarch, TorchComms, Helion, and OpenEnv.

## Principles

1. **Built for Scale**: Architected for massive workloads, supporting thousands of GPUs.
2. **PyTorch-Native**: Deeply integrated into the PyTorch ecosystem.
3. **Heterogeneous Hardware Ready**: From edge devices to data centers.

## The Stack

- **Helion**: A Python-embedded DSL for authoring ML kernels, reducing code by 4x compared to Triton.
- **Torchcomms**: A unified API for fault-tolerant distributed communication across 100,000+ GPUs.
- **Monarch**: A distributed execution engine reimagining cluster-scale orchestration.
- **Torchforge**: A PyTorch-native library for scalable RL post-training and agentic development.
- **ExecuTorch 1.0**: End-to-end on-device AI solution, now GA.
- **OpenEnv**: An open hub and spec for RL environments, launched with Hugging Face.

All projects are available now and open to contributions at meta-pytorch.org.