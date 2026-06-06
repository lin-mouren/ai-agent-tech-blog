---
title: "Learning to Watermark in the Latent Space of Generative Models (DistSeal)"
vendor: meta
source_url: https://ai.meta.com/research/publications/learning-to-watermark-in-the-latent-space-of-generative-models/
published_at: 2025-12-18
tags: [watermarking, latent-space, diffusion-models, autoregressive-models, provenance, DistSeal, generative-AI]
---

# Learning to Watermark in the Latent Space of Generative Models

**December 18, 2025** | Meta AI Research

## Overview

Existing approaches for watermarking AI-generated outputs often rely on post-hoc methods applied in pixel space, introducing computational overhead and potential visual artifacts. This work explores **latent space watermarking** and its distillation into generative models.

The paper introduces **DistSeal**: a unified approach for latent watermarking that works across both diffusion and autoregressive models.

## Key Technical Contributions

### Latent Domain Watermarking
Demonstrates that post-hoc watermarking methods can be applied directly in the latent domain (instead of pixel space), offering:
- Better imperceptibility
- Significantly reduced computational cost

### Distillation into Generative Models
Latent watermarkers can be effectively distilled into the generative pipeline:
- Into the generative model itself, **or**
- Into the latent decoder

This enables **in-model watermarking** where the watermark is baked in at generation time.

## Results

| Method | Robustness | Imperceptibility | Speed |
|---|---|---|---|
| Pixel-space post-hoc | Baseline | Baseline | Baseline |
| Latent post-hoc | Comparable | Better | **20× faster** |
| Distilled latent | Better | Better | Even faster |

Key finding: **Distilling latent watermarkers outperforms distilling pixel-space ones**, providing a solution that is both more efficient and more robust.

## Why This Matters

As generative AI scales, reliable watermarking at generation time (rather than as a post-processing step) becomes increasingly important for:
- Content provenance
- AI-generated content labeling
- Platform accountability

By working in latent space, DistSeal achieves the efficiency needed for production-scale deployment.

## Code and Models

Code and models will be available at [github.com/facebookresearch/distseal](https://github.com/facebookresearch/distseal)

Published on arXiv
