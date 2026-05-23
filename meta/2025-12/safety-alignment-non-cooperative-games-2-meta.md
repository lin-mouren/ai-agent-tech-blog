---
title: "Safety Alignment of LMs via Non-cooperative Games"
vendor: meta
source_url: https://ai.meta.com/research/publications/safety-alignment-of-lms-via-non-cooperative-games/
published_at: 2025-12-26T00:00:00.000Z
crawled_at: 2026-05-23T14:59:27.000Z
word_count: 800
reading_time_minutes: 4
tags: [safety, alignment, reinforcement-learning, adversarial, research]
---

# Safety Alignment of LMs via Non-cooperative Games

December 26, 2025

Ensuring the safety of language models (LMs) while maintaining their usefulness remains a critical challenge in AI alignment. Current approaches rely on sequential adversarial training: generating adversarial prompts and fine-tuning LMs to defend against them.

## A new paradigm

We introduce a different paradigm: framing safety alignment as a non-zero-sum game between an Attacker LM and a Defender LM trained jointly via online reinforcement learning. Each LM continuously adapts to the other's evolving strategies, driving iterative improvement.

Our method uses a preference-based reward signal derived from pairwise comparisons instead of point-wise scores, providing more robust supervision and potentially reducing reward hacking.

## AdvGame: Shifting the Pareto frontier

Our RL recipe, AdvGame, shifts the Pareto frontier of safety and utility, yielding a Defender LM that is simultaneously more helpful and more resilient to adversarial attacks. In addition, the resulting Attacker LM converges into a strong, general-purpose red-teaming agent that can be directly deployed to probe arbitrary target models.

This work represents a promising new direction for safety alignment that goes beyond sequential adversarial training by framing the problem as a dynamic game between attacker and defender.