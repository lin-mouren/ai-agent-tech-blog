---
title: "SAM 3 and SAM 3D: Next-Generation Segment Anything Models for Vision and 3D Reconstruction"
date: 2025-11-19
vendor: meta
tags: [SAM, computer-vision, 3D-reconstruction, segmentation, object-detection, open-source]
source: https://about.fb.com/news/2025/11/new-sam-models-detect-objects-create-3d-reconstructions/
---

# SAM 3 and SAM 3D: Next-Generation Segment Anything Models for Vision and 3D Reconstruction

**Date:** November 19, 2025  
**Vendor:** Meta (FAIR)  
**Source:** https://about.fb.com/news/2025/11/new-sam-models-detect-objects-create-3d-reconstructions/

## Overview

Meta released SAM 3 and SAM 3D, two major updates to the Segment Anything collection. SAM 3 enables detection and tracking of objects in images and video using text and visual prompts. SAM 3D enables 3D reconstruction of objects and people from a single image. Together they advance AI understanding from 2D pixel-level segmentation to full spatial 3D reconstruction.

## SAM 3

- **Capability:** Detects and tracks objects across images and video with text or visual (click) prompts
- **New:** Adds text prompt support — type "yellow school bus" and it finds, segments, and tracks through every frame
- **Availability:** Segment Anything Playground (web demo)
- **Use cases:** Video editing, content creation, annotation tools, augmented reality

## SAM 3D

Consists of two specialized models:

### SAM 3D Objects
- Enables object and scene 3D reconstruction from single 2D images
- Sets new standard for grounded 3D reconstruction in physical world scenarios
- Benchmarked on new SA-3DAO dataset (SAM 3D Artist Objects) — diverse paired images and meshes

### SAM 3D Body
- Focuses on human body and shape estimation from single images
- State-of-the-art performance on body reconstruction benchmarks

## Segment Anything Playground

New platform launched alongside SAM 3 and SAM 3D allowing anyone to:
- Upload their own images
- Select humans and objects
- Generate detailed 3D reconstructions
- Try SAM Audio (see December 2025 release)

## Open Source

- SAM 3D model checkpoints and inference code available publicly
- SA-3DAO dataset released as novel 3D reconstruction evaluation benchmark
- Integration with Roboflow annotation platform for custom use cases

## Resources

- About Meta: https://about.fb.com/news/2025/11/new-sam-models-detect-objects-create-3d-reconstructions/
- AI at Meta blog (SAM 3D): https://ai.meta.com/blog/sam-3d/
