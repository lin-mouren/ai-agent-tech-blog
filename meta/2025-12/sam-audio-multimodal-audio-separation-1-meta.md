---
title: "Introducing SAM Audio: The First Unified Multimodal Model for Audio Separation"
vendor: meta
source_url: https://ai.meta.com/blog/sam-audio/
published_at: 2025-12-16T00:00:00.000Z
crawled_at: 2026-05-23T14:59:27.000Z
word_count: 1400
reading_time_minutes: 7
tags: [audio, segmentation, multimodal, sam, foundation-model]
---

# Introducing SAM Audio: The First Unified Multimodal Model for Audio Separation

December 16, 2025

We're introducing SAM Audio, a state-of-the-art unified model that uses intuitive and multimodal prompts for audio separation. Just as Meta's Segment Anything Model (SAM) revolutionized computer vision by enabling people to segment any object in images and videos, SAM Audio transforms audio processing by making it easy to isolate any sound from complex audio mixtures.

## How it works

SAM Audio uses natural, multimodal prompts—whether through text, visual cues, or marking time segments—to isolate specific sounds from complex mixtures. This intuitive approach mirrors how people naturally engage with sound, making audio separation more accessible and useful than ever before.

At the heart of SAM Audio is Perception Encoder Audiovisual (PE-AV), a technical engine built on the open source Perception Encoder model. PE-AV enables the building of more advanced computer vision systems that can assist people in everyday tasks, including sound detection.

## Key components

Alongside SAM Audio, we're sharing:
- **SAM Audio-Bench**: The first in-the-wild audio separation benchmark
- **SAM Audio Judge**: The first automatic judge model for audio separation
- **PE-AV**: The technical engine that helps SAM Audio achieve state-of-the-art performance

## Performance

Built on a flow-matching transformer architecture, SAM Audio is trained on large-scale multimodal mixtures spanning speech, music, and general sounds. The model achieves state-of-the-art performance across a diverse suite of benchmarks, including general sound, speech, music, and musical instrument separation in both in-the-wild and professionally produced audios.

## Availability

SAM Audio and PE-AV are available starting now. Try SAM Audio by visiting the Segment Anything Playground where you can explore the capabilities of our new model, along with SAM 3 and SAM 3D.