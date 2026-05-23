---
title: "Introducing gpt-oss-safeguard"
vendor: openai
source_url: https://openai.com/index/introducing-gpt-oss-safeguard/
published_at: 2025-10-29T00:00:00.000Z
crawled_at: 2026-05-23T14:44:14.000Z
word_count: 1800
reading_time_minutes: 9
tags: [safety, open-source, reasoning-models, OpenAI]
---

October 29, 2025

# Introducing gpt-oss-safeguard

New open safety reasoning models (120b and 20b) that support custom safety policies.

Today, we're releasing a research preview of gpt-oss-safeguard, our open-weight reasoning models for safety classification tasks, available in two sizes: gpt-oss-safeguard-120b and gpt-oss-safeguard-20b. These models are fine-tuned versions of our gpt-oss open models and available under the same permissive Apache 2.0 license.

The gpt-oss-safeguard models use reasoning to directly interpret a developer-provided policy at inference time—classifying user messages, completions, and full chats according to the developer's needs. The developer always decides what policy to use, so responses are more relevant and tailored to the developer's use case. The model uses chain-of-thought, which the developer can review to understand how the model is reaching its decisions.

## System-level safety

When it comes to safety, we believe in defense in depth. Safety classifiers, which distinguish safe from unsafe content in a particular risk area, have long been a primary layer of defense. gpt-oss-safeguard is different because its reasoning capabilities allow developers to apply any policy, including ones they write themselves.

## How we use safety reasoning internally

Our primary reasoning models now learn our safety policies directly and use their reasoning capabilities to reason about what's safe. This approach, which we call deliberative alignment, significantly improves on earlier safety training methods.

Safety Reasoner has become a core component of our safety stack. For image generation and Sora 2, it performs dynamic, step-wise evaluations of outputs to identify and block unsafe generations in real time.

## Performance

Our gpt-oss-safeguard models and internal Safety Reasoner outperform gpt-5-thinking and the gpt-oss open models on multi-policy accuracy across internal and external evaluations.

## Limitations

Classifiers trained on tens of thousands of high-quality labeled samples can still perform better at classifying content than gpt-oss-safeguard. Also, gpt-oss-safeguard can be time and compute-intensive.
