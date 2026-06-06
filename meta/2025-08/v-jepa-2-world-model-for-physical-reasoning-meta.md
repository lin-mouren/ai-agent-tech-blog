---
title: "Introducing V-JEPA 2: World Model for Physical Reasoning and Robotics"
date: 2025-06-11
vendor: meta
tags: [world-model, robotics, video-understanding, self-supervised-learning, V-JEPA]
source: https://ai.meta.com/blog/v-jepa-2-world-model-benchmarks
---

# Introducing V-JEPA 2: World Model for Physical Reasoning and Robotics

**Date:** June 11, 2025  
**Vendor:** Meta (FAIR)  
**Source:** https://ai.meta.com/blog/v-jepa-2-world-model-benchmarks

## Overview

Meta's Fundamental AI Research (FAIR) team released V-JEPA 2, the successor to the V-JEPA video understanding model. V-JEPA 2 is a self-supervised foundation world model trained on over 1 million hours of video data that achieves state-of-the-art performance on visual understanding and physical prediction tasks. It represents a major step in Meta's push toward Advanced Machine Intelligence (AMI) — AI agents that can operate in the physical world.

## Key Features

- **World Model Architecture:** Uses Joint Embedding Predictive Architecture (JEPA) to learn predictions in representation space rather than pixel space, learning high-level physical dynamics
- **Two-Stage Training:** Stage 1 is self-supervised learning from 1M+ hours of video and 1M images; Stage 2 introduces action-conditioned learning from ~62 hours of robot control data
- **Zero-Shot Robot Planning:** Can be used for zero-shot robot planning with unfamiliar objects in new environments, outperforming Cosmos (NVIDIA's video generation model) on manipulation tasks
- **New Benchmarks Released:** Meta released 3 new benchmarks for evaluating physical world understanding from video
- **Open Source:** Model checkpoints released publicly on Hugging Face (facebook/vjepa2 collection)

## Model Sizes

- ViT-L (0.3B parameters)
- ViT-H (0.7B parameters)
- ViT-g (1B parameters, best performance)

## Performance Highlights

- V-JEPA 2 ViT-g achieves 87.5 average performance across image and video encoder benchmarks
- Significantly outperforms other vision encoders on motion understanding tasks
- In robotics tasks: 100% reach success rate, 80% cup pick-and-place (vs 0% for Cosmos baseline)
- Trained only on 62 hours of robot data vs Cosmos trained on 20M hours of video

## Significance

V-JEPA 2 directly advances Yann LeCun's vision of world models as the path to true AI that understands physical reality. It represents the convergence of large-scale video understanding with practical robotics planning, laying groundwork for autonomous AI agents that can operate without vast robotic training data.

## Resources

- Blog: https://ai.meta.com/blog/v-jepa-2-world-model-benchmarks
- Research page: https://ai.meta.com/research/vjepa
- Paper: https://arxiv.org/abs/2506.09985
- HuggingFace: https://huggingface.co/collections/facebook/v-jepa-2
