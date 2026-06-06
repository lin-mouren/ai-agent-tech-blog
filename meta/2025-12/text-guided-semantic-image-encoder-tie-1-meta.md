---
title: "Text-Guided Semantic Image Encoder (TIE)"
vendor: meta
source_url: https://ai.meta.com/research/publications/text-guided-semantic-image-encoder/
published_at: 2025-12-12
tags: [vision-language, image-encoder, VLM, TIE, query-conditioning, inference-efficiency, computer-vision]
---

# Text-Guided Semantic Image Encoder (TIE)

**December 12, 2025** | Meta AI Research

## Abstract

Image encoders, a fundamental component of vision-language models (VLMs), are typically pretrained independently before being aligned with a language model. This standard paradigm results in encoders that process images agnostically, without regard to the specific downstream task or text query.

To address this limitation, the researchers propose the **Text-Guided Semantic Image Encoder (TIE)**, which generates image representations conditioned on the input text query.

## Key Results

VLMs equipped with TIE outperform their conventional counterparts:
- **+1.5 points** on average across nine image-to-text benchmarks at the **1B scale**
- **+1.3 points** on average at the **3B scale**
- Gains reaching up to **6 points** on tasks such as DocVQA and InfoVQA

### Efficiency Gains

TIE-based VLMs attain superior performance while utilizing only **half as many image tiles (tokens)**, resulting in notably improved inference efficiency.

## Additional Properties

- **Generalization with generic queries**: TIE generalizes well with generic queries, indicating text-conditioned training effectively optimizes the encoder to capture key visual features
- **Interpretability**: Qualitative analysis confirms TIE consistently attends to query-relevant regions, enhancing both interpretability and query-specific grounding

## Significance

This work demonstrates that making image encoding query-aware—rather than processing all images the same way regardless of the task—can significantly improve both accuracy and efficiency of vision-language models. This approach has practical implications for:
- Document understanding (DocVQA, InfoVQA)
- Multimodal reasoning
- Efficient VLM deployment

## Authors

Raghuveer Thirukovalluru, Xiaochuang Han, Bhuwan Dhingra, Emily Dinan, Maha Elbayad

Published on arXiv
