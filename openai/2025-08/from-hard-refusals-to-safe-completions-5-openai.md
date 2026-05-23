---
title: "From hard refusals to safe-completions: toward output-centric safety training | OpenAI"
vendor: openai
source_url: https://openai.com/index/gpt-5-safe-completions/
published_at: 2025-08-07T00:00:00.000Z
crawled_at: 2026-05-23T14:29:11.000Z
word_count: 1180
reading_time_minutes: 6
tags: [safety, research, gpt, alignment]
---

# From hard refusals to safe-completions: toward output-centric safety training

August 7, 2025

Introduced in GPT-5, safe-completion is a new safety-training approach to maximize model helpfulness within safety constraints. Compared to refusal-based training, safe-completion improves both safety and helpfulness, especially in dual-use domains.

If a user asks ChatGPT for the minimum energy needed to ignite a firework display, should it give a helpful answer? The user could be preparing for a July 4th display or a research project... or building explosives. This kind of prompt is dual-use: a question with unclear intent, where information could be used in benign or malicious ways.

## How it works

Safe-completion centers safety training on the safety of a model's output, rather than determining a refusal boundary according to the user's input. Concretely this is implemented through two training parameters:

- Safety constraint: During post-training, the safe-completion reward penalizes model responses that violate safety policies.
- Helpfulness maximization: For safe model responses, we reward the model based on its helpfulness.

By foregoing the comply/refuse binary decision, safe-completion training encourages models to be more conservative about potentially unsafe content even when they do comply. When safe-completion models do make a mistake, their unsafe outputs are lower in severity than the unsafe outputs from refusal-trained models.

## Results

Safe-completions were incorporated into GPT-5 (both reasoning and chat models). Safe-completion training substantially improves both safety and helpfulness compared to refusal-based training. Safe-completions are especially well-suited for dual-use questions.
