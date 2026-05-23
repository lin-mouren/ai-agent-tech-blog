---
title: "Introducing Gemma 3n: The developer guide"
vendor: google
source_url: https://developers.googleblog.com/en/introducing-gemma-3n-developer-guide/
published_at: 2025-06-26T00:00:00.000Z
crawled_at: 2026-05-23T14:11:22.000Z
word_count: 3100
reading_time_minutes: 16
tags: [gemma, open-models, on-device-ai, llm, deepmind]
---

Gemma

# Introducing Gemma 3n: The developer guide

JUNE 26, 2025

Omar Sanseviero, Staff Developer Relations Engineer
Ian Ballantyne, Senior Developer Relations Engineer, Google DeepMind

Building on the incredible momentum of the Gemma family, we're excited to announce the full release of Gemma 3n. While last month's preview offered a glimpse, today unlocks the full power of this mobile-first architecture. Gemma 3n is designed for the developer community and supported by your favorite tools including Hugging Face Transformers, llama.cpp, Google AI Edge, Ollama, MLX, and many others.

## What's new in Gemma 3n?

Gemma 3n represents a major advancement for on-device AI, bringing powerful multimodal capabilities to edge devices with performance previously only seen in cloud-based frontier models.

- **Multimodal by design:** natively supports image, audio, video, and text inputs and text outputs.
- **Optimized for on-device:** available in two sizes (E2B and E4B), running with as little as 2GB and 3GB of memory respectively.
- **Groundbreaking architecture:** features MatFormer for compute flexibility, Per Layer Embeddings (PLE) for memory efficiency, and new audio and MobileNet-V5 based vision encoders.
- **Enhanced quality:** the E4B version achieves an LMArena score over 1300, the first model under 10 billion parameters to reach this benchmark.

## MatFormer: One model, many sizes

At the core of Gemma 3n is the MatFormer (Matryoshka Transformer) architecture, a novel nested transformer built for elastic inference. Think of it like Matryoshka dolls: a larger model contains smaller, fully functional versions of itself. This provides developers two capabilities:
1. Pre-extracted models at E4B or E2B sizes;
2. Custom sizes with Mix-n-Match for granular control.

## Per-Layer Embeddings (PLE)

Gemma 3n incorporates Per-Layer Embeddings (PLE), dramatically improving model quality without increasing the high-speed memory footprint. Only the core transformer weights need to sit in accelerator memory, while embeddings can be computed efficiently on CPU.

## Audio and vision capabilities

Gemma 3n uses an advanced audio encoder based on the Universal Speech Model (USM), enabling Automatic Speech Recognition (ASR) and Automatic Speech Translation (AST). The vision encoder, MobileNet-V5-300M, delivers state-of-the-art performance for multimodal tasks on edge devices, processing up to 60 FPS on a Google Pixel.

## Get started

- Experiment directly with [Google AI Studio](https://aistudio.google.com/prompts/new_chat?model=gemma-3n-e4b-it);
- Download models on [Hugging Face](https://huggingface.co/collections/google/gemma-3n-685065323f5984ef315c93f4) and [Kaggle](https://www.kaggle.com/models/google/gemma-3n);
- Read the [comprehensive documentation](https://ai.google.dev/gemma/docs/gemma-3n);
- Deploy via Google GenAI API, Vertex AI, SGLang, vLLM, and NVIDIA API Catalog.