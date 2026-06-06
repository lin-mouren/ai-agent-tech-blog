---
title: "Pixel Seal: Adversarial-only training for invisible image and video watermarking"
vendor: meta
source_url: https://ai.meta.com/research/publications/pixel-seal-adversarial-only-training-for-invisible-image-and-video-watermarking/
published_at: 2025-12-18
tags: [watermarking, provenance, content-authentication, adversarial-training, computer-vision, imperceptibility]
---

# Pixel Seal: Adversarial-only training for invisible image and video watermarking

**December 18, 2025** | Meta AI Research

## Overview

Invisible watermarking is essential for tracing the provenance of digital content. **Pixel Seal** sets a new state-of-the-art for image and video watermarking by addressing three fundamental issues in existing methods.

## Problems with Existing Methods

1. **Unreliable perceptual losses**: Reliance on proxy perceptual losses (MSE, LPIPS) that fail to mimic human perception and result in visible watermark artifacts
2. **Optimization instability**: Conflicting objectives causing instability that necessitates exhaustive hyperparameter tuning
3. **Resolution scaling issues**: Reduced robustness and imperceptibility when scaling models to high-resolution images and videos

## Pixel Seal's Solutions

### Adversarial-Only Training Paradigm
Eliminates unreliable pixel-wise imperceptibility losses entirely. Instead, trains purely adversarially so the model learns what is and isn't perceptible to humans.

### Three-Stage Training Schedule
Stabilizes convergence by decoupling robustness and imperceptibility across three distinct phases.

### High-Resolution Adaptation
Addresses the resolution gap via:
- JND-based (Just Noticeable Difference) attenuation
- Training-time inference simulation to eliminate upscaling artifacts

### Video Extension
Adapts efficiently to video via **temporal watermark pooling**, making Pixel Seal a practical and scalable solution for video provenance.

## Results

Pixel Seal shows clear improvements over state-of-the-art across:
- Different image types
- A wide range of transformations (geometric, color, compression)

## Significance

As AI-generated content proliferates, reliable invisible watermarking becomes increasingly critical for:
- Content provenance tracking
- Copyright protection
- Deepfake detection
- Platform content moderation

Pixel Seal's adversarial-only approach represents a significant methodological advance that better aligns with actual human perception rather than proxy metrics.

## Authors

Alexandre Mourachko, Hady Elsahar, Pierre Fernandez, Sylvestre Rebuffi, Tom Sander, Tomáš Souček, Tuan Tran, Valeriu Lacatusu

Published on arXiv
