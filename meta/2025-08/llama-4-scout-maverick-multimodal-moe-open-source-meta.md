---
title: "Llama 4: Natively Multimodal MoE Models with 10M Token Context Window"
date: 2025-04-05
vendor: meta
tags: [llama-4, multimodal, MoE, mixture-of-experts, open-source, long-context, Scout, Maverick, Behemoth]
source: https://techcrunch.com/2025/04/05/meta-releases-llama-4-a-new-crop-of-flagship-ai-models/
---

# Llama 4: Natively Multimodal MoE Models with 10M Token Context Window

**Date:** April 5, 2025  
**Vendor:** Meta  
**Source:** https://techcrunch.com/2025/04/05/meta-releases-llama-4-a-new-crop-of-flagship-ai-models/

## Overview

Meta released Llama 4, its most capable open-weight model family. Released on a Saturday with little warning, Llama 4 introduced Mixture-of-Experts (MoE) architecture and native multimodality to the Llama ecosystem for the first time. Three models were announced: Scout, Maverick, and Behemoth (still training at release).

## Models Released

### Llama 4 Scout (17Bx16E)
- **Active params:** 17B | **Total params:** 109B
- **Architecture:** MoE with 16 experts
- **Context window:** 10 million tokens (unprecedented for open-source)
- **Runs on:** Single H100 GPU (with int4 quantization)
- **Best for:** Long document analysis, codebase reasoning, document summarization
- **Knowledge cutoff:** August 2024

### Llama 4 Maverick (17Bx128E)
- **Active params:** 17B | **Total params:** ~400B
- **Architecture:** MoE with 128 experts, visual grounding-optimized
- **Context window:** 1 million tokens
- **Best for:** General assistant, creative writing, chat, multimodal reasoning
- **Competes with:** GPT-4o, Gemini 2.0 Flash (not yet Gemini 2.5 Pro)
- **Knowledge cutoff:** August 2024

### Llama 4 Behemoth (still training at launch)
- **Active params:** 288B | **Total params:** ~2 trillion
- **Role:** Teacher model for training Scout and Maverick
- **Architecture:** MoE with 16 experts
- **Status:** State-of-the-art for math, multilingual, and image tasks among non-reasoning models

## Technical Innovations

- **Native Multimodality via Early Fusion:** Integrates text and vision tokens in shared unified architecture during pre-training (vs. adapter-based approaches)
- **MetaCLIP Vision Encoder:** New Meta vision encoder for better image-to-token representation
- **40T Token Training:** Trained on ~40 trillion tokens covering 200 languages
- **MoE Architecture:** First Llama models using Mixture-of-Experts for compute efficiency

## Release Notes & Controversy

- **EU Restriction:** Multimodal features not available to EU-based users due to regulatory uncertainty
- **Benchmark Questions:** An experimental variant briefly ranked #2 on LMSYS Chatbot Arena with unusually long emoji-heavy answers; confirmed to be a different chat variant from public release
- **Community Reception:** Mixed; some users found Scout's output quality degraded in very long contexts

## Integration

- Available: llama.com, Hugging Face
- Meta AI across WhatsApp, Messenger, Instagram: Updated to use Llama 4 in 40 countries at launch
- Partners: Goldman Sachs, AT&T, DoorDash, NVIDIA, Snowflake, and 25+ others

## Resources

- TechCrunch: https://techcrunch.com/2025/04/05/meta-releases-llama-4-a-new-crop-of-flagship-ai-models/
- HuggingFace blog: https://huggingface.co/blog/llama4-release
- VentureBeat: https://venturebeat.com/technology/metas-answer-to-deepseek-is-here-llama-4-launches
