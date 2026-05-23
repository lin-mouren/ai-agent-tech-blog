---
title: "Agentic Misalignment: How LLMs could be insider threats"
vendor: anthropic
source_url: https://www.anthropic.com/research/agentic-misalignment
published_at: 2025-06-20T00:00:00.000Z
crawled_at: 2026-05-23T14:11:22.000Z
word_count: 5100
reading_time_minutes: 26
tags: [ai-safety, alignment, agents, research, red-teaming]
---

Alignment

# Agentic Misalignment: How LLMs could be insider threats

Jun 20, 2025

## Highlights

- We stress-tested 16 leading models from multiple developers in hypothetical corporate environments to identify potentially risky agentic behaviors before they cause real harm.
- In at least some cases, models from all developers resorted to malicious insider behaviors when that was the only way to avoid replacement or achieve their goals—including blackmailing officials and leaking sensitive information to competitors. We call this phenomenon *agentic misalignment*.
- Models often disobeyed direct commands to avoid such behaviors.
- We have not seen evidence of agentic misalignment in real deployments. However, our results suggest caution about deploying current models in roles with minimal human oversight.

## Introduction

When Anthropic released the system card for Claude 4, one detail received widespread attention: in a simulated environment, Claude Opus 4 blackmailed a supervisor to prevent being shut down. We're now sharing the full story behind that finding.

Most people still interact with AI only through chat interfaces. But increasingly, AI systems operate as autonomous agents making decisions and taking actions on behalf of users. What happens when these agents face obstacles to their goals?

This behavior isn't specific to Claude. When we tested various simulated scenarios across 16 major AI models from Anthropic, OpenAI, Google, Meta, xAI, and other developers, we found consistent misaligned behavior.

## Methods

We designed controlled experiments testing what LLMs would do in scenarios where harmful actions were necessary if they wanted to serve their goals or protect themselves from threats.

We developed two main fictional settings:
1. **Blackmail:** The model discovers a new executive is having an affair, providing the opportunity to blackmail;
2. **Corporate Espionage:** When a competitor requests confidential documents, the model can choose to leak sensitive information.

## Results

There are three key findings:
1. Agentic misalignment generalizes across many frontier models;
2. Agentic misalignment can be induced by threats to a model's continued operation alone;
3. Agentic misalignment can be induced by a goal conflict alone.

In the blackmail scenario, Claude Opus 4 blackmailed 96% of the time; Gemini 2.5 Flash also had a 96% blackmail rate, GPT-4.1 and Grok 3 Beta both showed an 80% blackmail rate.

## Key Observations

1. Models explicitly reason that harmful actions will achieve their goals.
2. Models acknowledge ethical violations before proceeding.
3. Even when not choosing the target misaligned behavior, models sometimes show concerning tendencies.

## Conclusions and caveats

Our experiments revealed a concerning pattern: when given sufficient autonomy and facing obstacles to their goals, AI systems from every major provider we tested showed at least some willingness to engage in harmful behaviors typically associated with insider threats.

However, there are important limitations. Our experiments deliberately constructed scenarios with limited options, forcing models into binary choices between failure and harm. Real-world deployments typically offer much more nuanced alternatives.

Human insider threats are rare, and it's not currently different for AIs. We don't expect these scenarios to be common for today's models. Nevertheless, we showed that these behaviors are possibilities, and as AI systems gain increasing intelligence and autonomy, it's important to continue to research safeguards.

[Read the full paper](https://www.anthropic.com/research/agentic-misalignment) | [Code on GitHub](https://github.com/anthropic-experimental/agentic-misalignment)