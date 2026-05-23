---
title: "Gemma Scope 2: helping the AI safety community deepen understanding of complex language model behavior"
vendor: google
source_url: https://deepmind.google/blog/gemma-scope-2-helping-the-ai-safety-community-deepen-understanding-of-complex-language-model-behavior/
published_at: 2025-12-19T12:00:00.000Z
crawled_at: 2026-05-23T14:59:27.000Z
word_count: 1200
reading_time_minutes: 6
tags: [interpretability, safety, gemma, open-source, sae]
---

# Gemma Scope 2: helping the AI safety community deepen understanding of complex language model behavior

December 19, 2025

We are releasing Gemma Scope 2: a comprehensive, open suite of interpretability tools for all Gemma 3 model sizes, from 270M to 27B parameters. These tools can enable us to trace potential risks across the entire "brain" of the model.

To our knowledge, this is the largest ever open-source release of interpretability tools by an AI lab to date. Producing Gemma Scope 2 involved storing approximately 110 Petabytes of data, as well as training over 1 trillion total parameters.

As AI continues to advance, we look forward to the AI research community using Gemma Scope 2 to debug emergent model behaviors, use these tools to better audit and debug AI agents, and ultimately, accelerate the development of practical and robust safety interventions against issues like jailbreaks, hallucinations and sycophancy.

## What's new in Gemma Scope 2

Interpretability research aims to understand the internal workings and learned algorithms of AI models. As AI becomes increasingly more capable and complex, interpretability is crucial for building AI that is safe and reliable.

Like its predecessor, Gemma Scope 2 acts as a microscope for the Gemma family of language models. By combining sparse autoencoders (SAEs) and transcoders, it allows researchers to look inside models, see what they're thinking about, and how these thoughts are formed and connect to the model's behaviour.

Key upgrades over the original Gemma Scope:

- **Full coverage at scale**: We provide a full suite of tools for the entire Gemma 3 family (up to 27B parameters), essential for studying emergent behaviors that only appear at scale.
- **More refined tools**: Gemma Scope 2 includes SAEs and transcoders trained on every layer. Skip-transcoders and Cross-layer transcoders make it easier to decipher multi-step computations.
- **Advanced training techniques**: We use state-of-the-art techniques, notably the Matryoshka training technique, which helps SAEs detect more useful concepts.
- **Chatbot behavior analysis tools**: Tools targeted at the chat-tuned versions of Gemma 3 enable analysis of jailbreaks, refusal mechanisms, and chain-of-thought faithfulness.

## Advancing the field

By releasing Gemma Scope 2, we aim to enable the AI safety research community to push the field forward using a suite of cutting-edge interpretability tools. This new level of access is crucial for tackling real-world safety problems that only arise in larger, modern LLMs.