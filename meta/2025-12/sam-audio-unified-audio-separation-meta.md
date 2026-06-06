---
title: "SAM Audio: The First Unified Multimodal Model for Audio Separation"
date: 2025-12-16
vendor: meta
tags: [SAM, audio, audio-separation, multimodal, foundation-model, open-source]
source: https://ai.meta.com/blog/sam-audio
---

# SAM Audio: The First Unified Multimodal Model for Audio Separation

**Date:** December 16, 2025  
**Vendor:** Meta  
**Source:** https://ai.meta.com/blog/sam-audio

## Overview

Meta released SAM Audio, the first unified multimodal model for audio separation — extending the Segment Anything philosophy from images and video to sound. Just as SAM revolutionized computer vision by allowing users to segment any object with a click, SAM Audio lets users isolate any sound from complex audio mixtures using natural multimodal prompts.

## Three Prompt Modalities

1. **Text Prompts:** Describe the sound you want to isolate (e.g., "guitar solo", "dog barking", "traffic noise")
2. **Visual Prompts:** Use clicks/masks on video frames to identify sound sources visually
3. **Span Prompts:** Mark a specific time segment where the target sound is audible — first-of-its-kind for audio
4. **Multi-modal Combination:** All three modalities can be combined for maximum precision

## Technical Architecture

- **Core:** Diffusion transformer trained with flow matching on large-scale audio mixtures
- **Engine:** Perception Encoder Audiovisual (PE-AV), built on Meta's open-source Perception Encoder model
- **Coverage:** Speech, music (instrument/vocal isolation), and general environmental sounds
- **First Foundation Model:** Unifies all audio separation tasks into one model vs. previous fragmented specialist approaches

## Accompanying Releases

- **SAM Audio-Bench:** First in-the-wild audio separation benchmark
- **SAM Audio Judge:** First automatic judge model for evaluating audio separation quality
- **PE-AV (Perception Encoder Audiovisual):** Underlying audio-visual representation model

## Try It

Available on the Segment Anything Playground at meta.ai, alongside SAM 3 and SAM 3D. Model also available for download.

## Applications

- Music production: Isolate instruments, separate stems
- Film/TV post-production: Remove background noise, isolate dialogue
- Podcasting: Clean up interview audio
- Accessibility: Hearing assistance technology
- Scientific research: Bioacoustics, environmental monitoring
- AI training data: Clean up noisy audio training sets

## Resources

- Blog: https://ai.meta.com/blog/sam-audio
- Research page: https://ai.meta.com/research/samaudio
- About Meta: https://about.fb.com/news/2025/12/our-new-sam-audio-model-transforms-audio-editing
- ArXiv paper: https://arxiv.org/html/2512.18099v1
