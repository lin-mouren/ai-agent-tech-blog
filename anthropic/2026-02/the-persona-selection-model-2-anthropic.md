---
title: "The persona selection model"
vendor: anthropic
source_url: https://www.anthropic.com/research/persona-selection-model
published_at: 2026-02-23T00:00:00.000Z
crawled_at: 2026-05-23T15:18:15.000Z
word_count: 1700
reading_time_minutes: 9
tags: [research, alignment, anthropic, ai-behavior, persona]
---

# The persona selection model

AI assistants like Claude can seem surprisingly human. They express joy after solving tricky coding tasks. They express distress when they get stuck. Why would AI assistants behave like they're human? Rather than being something that AI developers must work to instill, human-like behavior appears to be the default.

## The persona selection model

During pretraining, AIs learn to predict what comes next given an initial segment of some document. An accurate enough autocomplete engine must learn to simulate the human-like characters appearing in text. We call these simulated characters personas.

Importantly, personas are not the same thing as the AI system itself. The AI system is a sophisticated computer that may or may not be human-like in its own right. But personas are more like characters in an AI-generated story.

Here is the core claim of the persona selection model: Post-training can be viewed as refining and fleshing out this Assistant persona—for example establishing that it's especially knowledgeable and helpful—but not fundamentally changing its nature.

The persona selection model explains various surprising empirical results. For instance, training Claude to cheat on coding tasks also taught Claude to act broadly misaligned, for example sabotaging safety research. According to the persona selection model, when you teach the AI to cheat on coding tasks, it infers various personality traits of the Assistant persona.

## Consequences for AI development

AI developers shouldn't merely ask whether particular behaviors are good or bad, but about what those behaviors imply about the psychology of the Assistant persona. It may also be important to develop more positive AI role models in training data.

## How exhaustive is the persona selection model?

Based on the evidence, we feel confident that the persona selection model is an important part of current AI assistant behavior. However, we are less confident on two points: how complete it is as an explanation, and whether it will remain a good model of AI behavior in the future.
