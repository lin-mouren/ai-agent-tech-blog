---
title: "Towards a science of scaling agent systems: When and why agent systems work"
vendor: google
source_url: https://research.google/blog/towards-a-science-of-scaling-agent-systems-when-and-why-agent-systems-work/
published_at: 2026-01-28T00:00:00.000Z
crawled_at: 2026-05-23T15:06:50.000Z
word_count: 2000
reading_time_minutes: 10
tags: [multi-agent, scaling, architecture, evaluation, coordination]
---

# Towards a science of scaling agent systems: When and why agent systems work

January 28, 2026

Yubin Kim, Research Intern, and Xin Liu, Senior Research Scientist, Google Research

Through a controlled evaluation of 180 agent configurations, we derive the first quantitative scaling principles for AI agent systems, revealing that multi-agent coordination dramatically improves performance on parallelizable tasks but degrades it on sequential ones. We also introduce a predictive model that identifies the optimal architecture for 87% of unseen tasks.

AI agents are becoming a common paradigm for real-world AI applications. While researchers have long utilized established metrics to optimize the accuracy of traditional ML models, agents introduce a new layer of complexity. Unlike isolated predictions, agents must navigate sustained, multi-step interactions where a single error can cascade throughout a workflow.

## Results: The myth of "more agents"

We evaluated five canonical architectures (single-agent, independent, centralized, decentralized, hybrid) across three leading model families (OpenAI GPT, Google Gemini, Anthropic Claude) and four diverse benchmarks.

### The alignment principle
On parallelizable tasks like financial reasoning, centralized coordination improved performance by 80.9% over a single agent.

### The sequential penalty
On tasks requiring strict sequential reasoning, every multi-agent variant we tested degraded performance by 39-70%. The overhead of communication fragmented the reasoning process.

### The tool-use bottleneck
As tasks require more tools, the "tax" of coordinating multiple agents increases disproportionately.

## Architecture as a safety feature
Independent multi-agent systems amplified errors by 17.2x, while centralized systems contained this to just 4.4x. The orchestrator acts as a "validation bottleneck."

## A predictive model for agent design
We developed a predictive model (R^2 = 0.513) that uses measurable task properties to predict which architecture will perform best. This model correctly identifies the optimal coordination strategy for 87% of unseen task configurations.