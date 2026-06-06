---
title: "Four MTIA Chips in Two Years: Meta's Custom Silicon Strategy for AI Inference"
date: 2026-03-11
vendor: meta
tags: [MTIA, hardware, silicon, AI-inference, chips, custom-silicon, infrastructure]
source: https://ai.meta.com/blog/meta-mtia-scale-ai-chips-for-billions/
---

# Four MTIA Chips in Two Years: Meta's Custom Silicon Strategy for AI Inference

**Date:** March 11, 2026  
**Vendor:** Meta  
**Source:** https://ai.meta.com/blog/meta-mtia-scale-ai-chips-for-billions/

## Overview

Meta announced four successive generations of its in-house Meta Training and Inference Accelerator (MTIA) chips, developed in partnership with Broadcom, scheduled for deployment within two years. This represents a roughly 6-month chip cadence — much faster than the industry's typical 1-2 year cycle.

## MTIA Generation Roadmap

| Chip | Status | Primary Use |
|------|--------|-------------|
| MTIA 300 | In production | Ranking & recommendations training |
| MTIA 400 | Lab testing (deploying 2026) | All workloads, focus on GenAI inference |
| MTIA 450 | Deploying early 2027 | GenAI inference (MX4 precision, 6x FP16 FLOPs) |
| MTIA 500 | Deploying late 2027 | GenAI inference (50% more HBM bandwidth vs 450) |

## Technical Highlights

- **From MTIA 300 to 500:** 4.5x increase in HBM bandwidth, 25x increase in compute FLOPs
- **MTIA 450:** Supports MX4 data type delivering 6x MX4 FLOPs vs FP16/BF16
- **MTIA 500:** 50% more HBM bandwidth than 450, further low-precision innovations
- **Same chassis/rack/network infrastructure** for 400, 450, 500 — modular drop-in replacement
- **Inference-first design:** Optimized for GenAI inference first, then applied to training

## Software Stack

- Native PyTorch support
- vLLM compatibility
- Triton kernel support
- torch.compile and torch.export: Deploy same production models on both GPUs and MTIA without rewrites
- Hundreds of thousands of MTIA chips already deployed across Meta's apps for organic content and ads

## Strategy

Unlike mainstream chips built for the most demanding workload (large-scale GenAI pre-training), MTIA chips are optimized inference-first for serving billions of users across Facebook, Instagram, WhatsApp. This "inference-first" philosophy keeps MTIA well-tuned to the anticipated growth in GenAI serving demand.

## Context

Meta's AI capex for 2026: $115-135 billion (nearly twice 2025). Custom silicon is central to making this infrastructure economically viable — each MTIA chip generation replaces expensive NVIDIA GPUs for inference workloads at Meta's scale.

## Resources

- Blog: https://ai.meta.com/blog/meta-mtia-scale-ai-chips-for-billions/
- About Meta: https://about.fb.com/news/2026/03/expanding-metas-custom-silicon-to-power-our-ai-workloads/
- Tom's Hardware: https://www.tomshardware.com/tech-industry/semiconductors/meta-reveals-four-new-mtia-chips-built-for-ai-inference
