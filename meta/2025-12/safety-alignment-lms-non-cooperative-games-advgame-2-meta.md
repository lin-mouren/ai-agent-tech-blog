---
title: "Safety Alignment of LMs via Non-cooperative Games (AdvGame)"
vendor: meta
source_url: https://ai.meta.com/research/publications/safety-alignment-of-lms-via-non-cooperative-games/
published_at: 2025-12-26
tags: [safety-alignment, reinforcement-learning, adversarial-training, game-theory, red-teaming, AdvGame]
---

# Safety Alignment of LMs via Non-cooperative Games

**December 26, 2025** | Meta AI Research

## Abstract

Ensuring the safety of language models (LMs) while maintaining their usefulness remains a critical challenge in AI alignment. Current approaches rely on sequential adversarial training: generating adversarial prompts and fine-tuning LMs to defend against them.

This work introduces a different paradigm: framing safety alignment as a **non-zero-sum game between an Attacker LM and a Defender LM** trained jointly via online reinforcement learning.

## Key Innovation: AdvGame

The RL recipe, **AdvGame**, works as follows:

1. **Attacker LM** continuously generates adversarial prompts
2. **Defender LM** is trained to respond safely and helpfully
3. Each LM continuously adapts to the other's evolving strategies, driving iterative improvement
4. A **preference-based reward signal** derived from pairwise comparisons (instead of point-wise scores) provides more robust supervision

## Results

AdvGame shifts the **Pareto frontier of safety and utility**, yielding:

- **Defender LM**: simultaneously more helpful AND more resilient to adversarial attacks
- **Attacker LM**: converges into a strong, general-purpose red-teaming agent that can be directly deployed to probe arbitrary target models

## Advantages Over Sequential Adversarial Training

| Feature | Sequential Approach | AdvGame |
|---|---|---|
| Training | Two-stage (attack then defend) | Joint (simultaneous) |
| Reward Signal | Point-wise scores | Pairwise comparisons |
| Reward Hacking | More susceptible | More robust |
| Attack Quality | Static once trained | Continuously improving |

## Significance

This game-theoretic approach to safety alignment represents a fundamental shift from treating safety as a "patch" applied after training to integrating it as a core dynamic throughout the training process. The resulting attacker LM also has standalone value as a red-teaming tool for safety evaluation of other models.

## Authors

Brandon Amos, Anselm Paulus, Ilia Kulikov, Ivan Evtimov, Kamalika Chaudhuri, Remi Munos, Arman Zharmagambetov

Published on arXiv
