---
title: "Pixel Seal: Adversarial-only training for invisible image and video watermarking"
vendor: meta
source_url: https://ai.meta.com/research/publications/pixel-seal-adversarial-only-training-for-invisible-image-and-video-watermarking/
published_at: 2025-12-18T00:00:00.000Z
crawled_at: 2026-05-23T14:59:27.000Z
word_count: 900
reading_time_minutes: 5
tags: [watermarking, computer-vision, security, ai-generated-content, research]
---

# Pixel Seal: Adversarial-only training for invisible image and video watermarking

December 18, 2025

Invisible watermarking is essential for tracing the provenance of digital content. However, training state-of-the-art models remains notoriously difficult, with current approaches often struggling to balance robustness against true imperceptibility.

## Key innovations

Pixel Seal sets a new state-of-the-art for image and video watermarking by addressing three fundamental issues of existing methods:

1. **Adversarial-only training**: Eliminates unreliable pixel-wise imperceptibility losses (like MSE and LPIPS) that fail to mimic human perception and result in visible watermark artifacts.

2. **Three-stage training schedule**: Stabilizes convergence by decoupling robustness and imperceptibility optimization, avoiding the conflicting objectives that necessitate exhaustive hyperparameter tuning.

3. **Resolution gap via high-resolution adaptation**: Employs JND-based attenuation and training-time inference simulation to eliminate upscaling artifacts, enabling the model to work at high resolutions without quality loss.

## Results

Pixel Seal demonstrates clear improvements over the state-of-the-art across different image types and a wide range of transformations. The model efficiently adapts to video via temporal watermark pooling, positioning Pixel Seal as a practical and scalable solution for reliable provenance in real-world image and video settings.