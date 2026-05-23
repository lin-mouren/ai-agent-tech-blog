---
title: "Mapping the World's Forests with Greater Precision: Introducing Canopy Height Maps v2"
vendor: meta
source_url: https://ai.meta.com/blog/world-resources-institute-dino-canopy-height-maps-v2/
published_at: 2026-03-10T00:00:00.000Z
crawled_at: 2026-05-23T15:30:04.000Z
word_count: 680
reading_time_minutes: 4
tags: [research, open-source, multimodal, science]
---

Computer Vision

# Mapping the World's Forests with Greater Precision: Introducing Canopy Height Maps v2

March 10, 2026

Forests are essential to life on Earth - storing carbon, sheltering wildlife, and shaping our climate. Today, in partnership with the World Resources Institute, we are announcing Canopy Height Maps v2 (CHMv2): an open source model and world-scale maps generated with it.

## Technical approach

At the heart of CHMv2 is DINOv3, Meta's self-supervised vision model, which brings unprecedented clarity and detail to forest mapping worldwide. DINOv3 learns robust visual features from large amounts of unlabeled imagery. By training on diverse satellite data, DINOv3 captures subtle visual cues that indicate tree height - shadows, textures, and crown shapes - without requiring millions of manually labeled examples.

Building on our original high-resolution canopy height maps released in 2024, CHMv2 delivers substantial improvements in accuracy, detail, and global consistency. The model's R-squared has soared from 0.53 to 0.86, delivering sharper canopy maps while minimizing bias for tall trees.

## Real-world impact

Our previous AI model and maps, CHMv1, are already supporting climate migration, restoration, and biodiversity efforts. In the United Kingdom, Forest Research is using these to transform how they monitor and manage Great Britain's forests. The European Commission's Joint Research Centre used CHMv1 in its Global Forest Cover map for 2020 research.

## Looking Ahead

CHMv2 represents a significant step forward, but challenges remain. We are continuing to improve predictions in regions where data is sparse, address viewing-geometry effects, and extend temporal coverage to better support change detection over time.