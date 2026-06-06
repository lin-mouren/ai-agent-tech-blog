---
title: "Introducing SAM Audio: The First Unified Multimodal Model for Audio Separation"
vendor: meta
source_url: https://ai.meta.com/blog/sam-audio/
published_at: 2025-12-16
tags: [SAM-audio, audio-separation, multimodal, PE-AV, computer-vision, audio-AI, segment-anything]
---

# Introducing SAM Audio: The First Unified Multimodal Model for Audio Separation

**December 16, 2025** | Meta AI

## Overview

Just as Meta's Segment Anything Model (SAM) revolutionized computer vision by enabling people to segment any object in images and videos, **SAM Audio** does the same for sound—isolating any sound from complex audio mixtures using natural, multimodal prompts.

### What's Released

- **SAM Audio** — state-of-the-art unified model for audio separation
- **Perception Encoder Audiovisual (PE-AV)** — the technical engine powering SAM Audio
- **SAM Audio-Bench** — first in-the-wild audio separation benchmark
- **SAM Audio Judge** — first automatic judge model for audio separation

## SAM Audio Capabilities

### Three Prompting Modalities

1. **Text prompting**: Type "dog barking" or "singing voice" to extract specific sounds
2. **Visual prompting**: Click on speaking persons or sounding objects in video to isolate their audio
3. **Span prompting**: An industry first—mark time segments where target audio occurs (e.g., filter all dog barking from an entire podcast)

### Architecture

- Generative modeling framework built on a **flow-matching diffusion transformer**
- Takes an audio mixture and one or more prompts, encodes them into a shared representation
- Generates target and residual audio tracks
- Operates **faster than real-time** (RTF ≈ 0.7) from 500M to 3B parameters

### Performance

- Significantly surpasses prior work in universal audio separation
- Matches the performance of the best domain-specific models across speech, music, and general sounds
- Mixed-modality prompting (combining text and span inputs) delivers even stronger outcomes

## Perception Encoder Audiovisual (PE-AV)

The "ears" that help SAM Audio function:
- Built on Meta Perception Encoder (open source, released April 2025)
- Extends advanced computer vision capabilities to audio
- Extracts frame-level video features and aligns them with audio representations
- Trained on over **100 million videos** using large-scale multimodal contrastive learning

## SAM Audio-Bench

A comprehensive audio separation benchmark:
- Covers all major audio domains: speech, music, and general sound effects
- Supports text, visual, and span prompt types
- Built using audio and video from high-quality sources
- Features rich, multimodal prompts with human-drawn visual masks, time markers, and text descriptions
- Pioneers **reference-free evaluation** (evaluates without needing isolated reference tracks)

## SAM Audio Judge

A novel evaluation framework:
- Reference-free, objective metric that evaluates segmented audio based on perceptual criteria
- Built on nine perceptual dimensions: recall, precision, faithfulness, overall quality, and more
- Enables fair comparison of audio separation models

## Current Limitations

- Audio as a prompt is not supported
- Complete audio separation without prompting is outside scope
- Separating highly similar audio events (e.g., isolating one singer from a chorus) remains challenging

## Partnerships

Meta has partnered with:
- **Starkey** (largest US hearing aid manufacturer) — exploring accessibility applications
- **2gether-International** (leading startup accelerator for disabled founders) — exploring accessibility use cases

SAM Audio is available in the **Segment Anything Playground**.
