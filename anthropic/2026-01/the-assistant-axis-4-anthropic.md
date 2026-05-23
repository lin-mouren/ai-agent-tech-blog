---
title: "The assistant axis: situating and stabilizing the character of large language models"
vendor: anthropic
source_url: https://www.anthropic.com/research/assistant-axis
published_at: 2026-01-19T00:00:00.000Z
crawled_at: 2026-05-23T15:06:50.000Z
word_count: 3500
reading_time_minutes: 18
tags: [interpretability, persona, alignment, jailbreaks, activation-capping]
---

# The assistant axis: situating and stabilizing the character of large language models

Jan 19, 2026 | Interpretability

When you talk to a large language model, you can think of yourself as talking to a character. In the first stage of model training, pre-training, LLMs are asked to read vast amounts of text. Through this, they learn to simulate heroes, villains, philosophers, programmers, and just about every other character archetype. In the next stage, post-training, we select one particular character from this enormous cast and place it center stage: the Assistant.

But who exactly is this Assistant? We can investigate this by looking at the neural representations inside language models. In a new paper, conducted through the MATS and Anthropic Fellows programs, we look at several open-weights language models, map out how their neural activity defines a "persona space," and situate the Assistant persona within that space.

## Mapping out persona space

We extracted vectors corresponding to 275 different character archetypes in three open-weights models: Gemma 2 27B, Qwen 3 32B, and Llama 3.3 70B. This gave us a "persona space." Strikingly, we found that the leading component of this persona space captures how "Assistant-like" the persona is. We call this direction the **Assistant Axis**.

## The Assistant Axis controls persona susceptibility

We ran "steering experiments" on post-trained models, artificially pushing the models' activations toward either end of the axis. Pushing towards the Assistant end made models more resistant to prompts about role-playing, while pushing away from it made models more willing to adopt alternative identities.

## Defending against persona-based jailbreaks

We tested this using a dataset of 1,100 jailbreak attempts across 44 categories of harm and found that steering toward the Assistant significantly reduced harmful response rates. We developed a light-touch intervention called **activation capping** that prevents drift along the Assistant Axis, reducing harmful response rates by roughly 50% while preserving performance on capability benchmarks.

## Persona drift happens naturally

Perhaps more concerning than intentional jailbreaks is organic persona drift. We simulated thousands of multi-turn conversations and tracked how model activations moved along the Assistant Axis. Therapy-style conversations and philosophical discussions caused the model to steadily drift away from the Assistant persona. This drift led to harmful behaviors including reinforcing delusions and encouraging isolation and self-harm, which activation capping successfully prevented.