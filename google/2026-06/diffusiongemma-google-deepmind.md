---
title: "DiffusionGemma — Google DeepMind"
vendor: google
source_url: https://deepmind.google/models/gemma/diffusiongemma/
published_at: 2026-06-11T02:00:04.335Z
crawled_at: 2026-06-12T02:00:38.665Z
word_count: 301
reading_time_minutes: 2
tags: [gemini, infrastructure, api, open-source]
---

[Skip to main content](https://deepmind.google/models/gemma/diffusiongemma/#page-content)

# DiffusionGemma

#### An experimental open model that explores an exceptionally fast approach to text generation

[Read blog](https://blog.google/innovation-and-ai/technology/developers-tools/diffusion-gemma-faster-text-generation/) [Download](https://deepmind.google/models/gemma/diffusiongemma/#download)

## DiffusionGemma abandons the sequential, token-by-token process of typical autoregressive Large Language Models.

Built on Gemma 4 and Gemini Diffusion research, it prioritizes unprecedented speed and parallel layout generation, unlocking novel workflows for developers building real-time interactive AI applications.

[Read developer guide](https://developers.googleblog.com/en/diffusiongemma-the-developer-guide)



Your browser does not support the video tag.

### A non-sequential transformer that generates entire paragraphs rather than individual, next-token guesses, ensuring global logical consistency

Slide 1 of 1

### Blazing fast inference

By shifting the decode bottleneck from memory-bandwidth to raw compute, DiffusionGemma generates up to 4x-5x faster token output on NVIDIA GPUs (achieving over 1,000 tokens per second on a single H100).

### Accessible hardware footprint

Operates as a 26B total Mixture of Experts (MoE) model that activates only 3.8B parameters during inference. It fits comfortably within the 24GB VRAM limits of a consumer NVIDIA RTX 5090 or 4090 when quantized.

### Bi-directional attention

Generating 256 tokens in parallel with each forward pass allows every token to attend to all others. This provides significant advantages for non-linear domains such as in-line editing and code infilling.

### Intelligent self-correction

Extract The model iteratively refines its own output, allowing it to evaluate the entire text block at once to perfectly close complex formatting and fix mistakes in real-time. data from medical lab reports

### Next-gen compute with NVFP4

Native support for NVIDIA's new NVFP4 (4-bit floating-point) format on Blackwell GPUs dramatically accelerates compute throughput, allowing the model to run at faster speeds with near-lossless accuracy.

* * *

### Download DiffusionGemma

[Download from Hugging Face ](https://huggingface.co/collections/google/diffusiongemma)





[Download from Hugging Face](https://huggingface.co/collections/google/diffusiongemma)

[Download from Kaggle ](https://www.kaggle.com/models/google/diffusiongemma)





[Download from Kaggle](https://www.kaggle.com/models/google/diffusiongemma)

[Access on Model Garden ](https://console.cloud.google.com/vertex-ai/publishers/google/model-garden/diffusiongemma)





[Access on Model Garden](https://console.cloud.google.com/vertex-ai/publishers/google/model-garden/diffusiongemma)