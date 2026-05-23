---
title: "DINOv3: Self-supervised learning for vision at unprecedented scale"
vendor: meta
source_url: https://ai.meta.com/blog/dinov3-self-supervised-vision-model/
published_at: 2025-08-14T00:00:00.000Z
crawled_at: 2026-05-23T14:29:11.000Z
word_count: 920
reading_time_minutes: 5
tags: [computer-vision, ssl, research, open-source]
---

# DINOv3: Self-supervised learning for vision at unprecedented scale

August 14, 2025

## Takeaways
- We're introducing DINOv3, which scales self-supervised learning for images to create universal vision backbones that achieve absolute state-of-the-art performance across diverse domains, including web and satellite imagery.
- DINOv3 backbones produce powerful, high-resolution image features that make it easy to train lightweight adapters.
- We've incorporated community feedback, shipping smaller models that outperform comparable CLIP-based derivatives.
- We're releasing the DINOv3 training code and pre-trained backbones under a commercial license.

Self-supervised learning (SSL) has emerged as the dominant paradigm in modern machine learning. Today, we're releasing DINOv3, a generalist, state-of-the-art computer vision model trained with SSL that produces superior high-resolution visual features. For the first time, a single frozen vision backbone outperforms specialized solutions on multiple long-standing dense prediction tasks including object detection and semantic segmentation.

DINOv3's breakthrough performance is driven by innovative SSL techniques that eliminate the need for labeled data, enabling us to scale training data to 1.7B images and model size to 7B parameters. This label-free approach enables applications where annotations are scarce, costly, or impossible.

## Scalable and efficient visual modeling

We built DINOv3 by training a 7x larger model on a 12x larger dataset than its predecessor, DINOv2. The DINOv3 backbone particularly shines on all dense prediction tasks, showing exceptional understanding of scene layout and underlying physics.

## A family of deployment-friendly models

We built a family of models spanning a large range of inference compute requirements. By distilling the ViT-7B model into smaller variants like ViT-B and ViT-L, DINOv3 outperforms comparable CLIP-based models. DINOv3 is already having real-world impact — the World Resources Institute uses it to monitor deforestation, and NASA's Jet Propulsion Laboratory uses DINO models for space exploration robots.