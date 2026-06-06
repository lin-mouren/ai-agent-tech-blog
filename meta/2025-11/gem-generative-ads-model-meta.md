---
title: "GEM: Meta's Generative Ads Recommendation Model — LLM-Scale Foundation Model for Advertising"
date: 2025-11-10
vendor: meta
tags: [ads, recommendation-system, foundation-model, GEM, LLM, monetization]
source: https://engineering.fb.com/2025/11/10/ml-applications/metas-generative-ads-model-gem-the-central-brain-accelerating-ads-recommendation-ai-innovation/
---

# GEM: Meta's Generative Ads Recommendation Model

**Date:** November 10, 2025  
**Vendor:** Meta  
**Source:** https://engineering.fb.com/2025/11/10/ml-applications/metas-generative-ads-model-gem-the-central-brain-accelerating-ads-recommendation-ai-innovation/

## Overview

Meta published details about GEM (Generative Ads Recommendation Model), its most advanced ads foundation model. GEM is the largest foundation model for recommendation systems in the industry, trained at the scale of large language models across thousands of GPUs. It uses an LLM-inspired paradigm for ad recommendations, fundamentally changing how Meta's advertising stack operates.

## Technical Architecture

- **Scale:** Trained across thousands of GPUs, comparable to LLM training scale
- **Architecture:** LLM-inspired paradigm with novel architectural innovations enabling efficient scaling laws
- **Training:** Multi-dimensional parallelism, custom GPU kernels, memory optimizations
- **Knowledge Transfer:** Post-training uses advanced techniques to amplify performance of downstream models across the entire ads stack

## Business Impact

- Deployed across Facebook and Instagram
- **5% increase in ad conversions on Instagram** since launch
- **3% increase in ad conversions on Facebook Feed** (Q2 results)
- Enables more relevant and personalized ad experiences

## Key Innovation

GEM delivers performance gains that scale cost-effectively with data and compute — unlike previous recommendation systems that required significant engineering per new use case. By acting as a teacher/knowledge transfer model for downstream systems, it amplifies performance across Meta's entire advertising ecosystem simultaneously.

## Resources

- Engineering blog: https://engineering.fb.com/2025/11/10/ml-applications/metas-generative-ads-model-gem-the-central-brain-accelerating-ads-recommendation-ai-innovation/
