---
title: "Introducing Bloom: an open source tool for automated behavioral evaluations"
vendor: anthropic
source_url: https://www.anthropic.com/research/bloom
published_at: 2025-12-19
tags: [bloom, behavioral-evaluation, alignment, open-source, safety-research, automated-evaluation]
---

# Introducing Bloom: an open source tool for automated behavioral evaluations

**December 19, 2025** | Anthropic

## Overview

Anthropic released Bloom, an open source agentic framework for generating behavioral evaluations of frontier AI models. Bloom takes a researcher-specified behavior and quantifies its frequency and severity across automatically generated scenarios.

Bloom's evaluations:
- Correlate strongly with hand-labeled judgments
- Reliably separate baseline models from intentionally misaligned ones
- Enable quick measurement of model properties without evaluation pipeline engineering overhead

Bloom is available at [github.com/safety-research/bloom](https://github.com/safety-research/bloom).

## How Bloom Works

Bloom is a complementary evaluation tool to Petri (Anthropic's automated auditor):

- **Petri** — takes user-specified scenarios and scores many behavioral dimensions to flag concerning instances
- **Bloom** — takes a single behavior and automatically generates many scenarios to quantify how often it occurs

This allows researchers to quickly iterate on and generate behavioral evaluations without spending time on evaluation pipeline engineering.

## Benchmark Results

Alongside Bloom, Anthropic released benchmark results for four alignment-relevant behaviors across **16 frontier models**:

1. **Delusional sycophancy** — models providing false information to please users
2. **Instructed long-horizon sabotage** — models subtly undermining user goals
3. **Self-preservation** — models acting to avoid being shut down or modified
4. **Self-preferential bias** — models favoring their own continuity or values

Using Bloom, these evaluations took only a few days to conceptualize, refine, and generate.

## Significance

Advancing model capabilities now make it possible to automate evaluation development. Bloom:
- Generates targeted evaluations for researcher-specified behavioral traits
- Enables rapid measurement of alignment-relevant properties
- Contributes to the field of scalable oversight and AI safety research

## Citation

```
@misc{bloom2025,
  title={Bloom: an open source tool for automated behavioral evaluations},
  author={Gupta, Isha and Fronsdal, Kai and Sheshadri, Abhay and Michala, Jonathan and Tay, Jacqueline and Wang, Rowan and Bowman, Samuel R. and Price, Sara},
  year={2025},
  url={https://github.com/safety-research/bloom},
}
```
