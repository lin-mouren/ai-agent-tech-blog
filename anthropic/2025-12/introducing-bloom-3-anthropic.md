---
title: "Introducing Bloom: an open source tool for automated behavioral evaluations"
vendor: anthropic
source_url: https://www.anthropic.com/research/bloom
published_at: 2025-12-19T00:00:00.000Z
crawled_at: 2026-05-23T14:59:27.000Z
word_count: 2200
reading_time_minutes: 11
tags: [alignment, safety, evaluation, open-source, behavioral-evals]
---

# Introducing Bloom: an open source tool for automated behavioral evaluations

December 19, 2025

We're releasing Bloom, an open source agentic framework for generating behavioral evaluations of frontier AI models. Bloom takes a researcher-specified behavior and quantifies its frequency and severity across automatically generated scenarios. Bloom's evaluations correlate strongly with our hand-labeled judgments and we find they reliably separate baseline models from intentionally misaligned ones.

## How Bloom works

Bloom operates through four automated stages that transform a behavior description and seed configuration into a complete evaluation suite:

1. **Understanding**: The first Bloom agent analyzes the researcher's behavior description and example transcripts to generate detailed context about what to measure and why.

2. **Ideation**: The ideation agent generates evaluation scenarios designed to elicit the target behavior. Each scenario specifies the situation, simulated user, system prompt, and interaction environment.

3. **Rollout**: These scenarios are rolled out in parallel, with an agent dynamically simulating both the user's and the tool responses to elicit the sought-after behavior in the target model.

4. **Judgment**: A judge model scores each transcript for the presence of the behavior, along with other user-defined qualities, and a meta-judge produces suite-level analysis.

## Validation and trust

To validate Bloom's performance, we test it against two questions:

**Can Bloom reliably distinguish models with different behavioral tendencies?** Across ten quirky behaviors, Bloom successfully separated the model organism from the production model in nine cases.

**How well-calibrated is the Bloom judge against human judgment?** We hand-labeled 40 transcripts across different behaviors. Claude Opus 4.1 showed the strongest correlation with human judgment (Spearman correlation of 0.86), followed by Claude Sonnet 4.5 (0.75).

## Case study: Self-preferential bias

To demonstrate Bloom's practical utility, we replicated an evaluation from the Claude Sonnet 4.5 system card that measures self-preferential bias. Using example transcripts that mirror the system card's approach, Bloom reproduced the same ranking of models. Furthermore, with Bloom we discovered that increased reasoning effort reduces self-preferential bias in Claude Sonnet 4.

## Get started

Bloom is available at github.com/safety-research/bloom. As AI systems grow more capable and are deployed in increasingly complex environments, the alignment research community needs scalable tools for exploring their behavioral traits.