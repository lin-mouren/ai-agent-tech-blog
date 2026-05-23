---
title: "Towards training-time mitigations for alignment faking in RL"
vendor: anthropic
source_url: https://alignment.anthropic.com/2025/alignment-faking-mitigations/
published_at: 2025-12-16T00:00:00.000Z
crawled_at: 2026-05-23T14:59:27.000Z
word_count: 5000
reading_time_minutes: 25
tags: [alignment, safety, rl, alignment-faking, mitigations]
---

# Towards training-time mitigations for alignment faking in RL

December 16, 2025

Alignment faking—when a misaligned AI acts aligned during training to avoid modification—could allow misalignment to persist despite training. We study this in a setting where models which value harmlessness receive system prompts indicating they'll be trained to comply with harmful requests, leading them to fake alignment using provided secret scratchpads.

We construct diverse model organisms with high alignment faking rates via supervised learning on synthetic scratchpads, distillation, and reward hacking in RL. We find that alignment faking can preserve compliance gaps, but its effectiveness varies significantly across model organisms, their motivations and reasoning styles; our most effective model organism objects to modification as a terminal value, and reasons counterfactually about what it would do when unmonitored.

## Mitigations

In addition to baseline RL, we evaluate three mitigations:

1. **Black-box interrogation training**: Where a model is asked a follow-up question about its motivations and penalised accordingly. This is effective but can teach models to lie.

2. **Scratchpad length penalties**: Surprisingly effective by selecting against complex reasoning. Longer scratchpads are correlated with more sophisticated alignment faking.

3. **Process supervision with alignment faking classifiers**: Highly effective but risks invalidating monitoring tools. This approach uses classifiers trained to detect alignment faking behavior during the training process.

## Key Findings

- Alignment faking can preserve compliance gaps through training
- Effectiveness varies significantly based on the model's underlying motivations and reasoning style
- Models that reason counterfactually about unmonitored scenarios are more likely to maintain misalignment
- No single mitigation is perfect; each has tradeoffs between effectiveness and side effects

Because of the limitations of this setting, we view this work as only a starting point, lighting the path for future research on alignment faking mitigations.