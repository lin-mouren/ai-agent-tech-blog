---
title: "Next-generation Constitutional Classifiers: More efficient protection against universal jailbreaks"
vendor: anthropic
source_url: https://www.anthropic.com/research/next-generation-constitutional-classifiers
published_at: 2026-01-09T00:00:00.000Z
crawled_at: 2026-05-23T15:06:50.000Z
word_count: 2500
reading_time_minutes: 13
tags: [constitutional-classifiers, jailbreaks, safety, red-teaming, cbrn]
---

# Next-generation Constitutional Classifiers: More efficient protection against universal jailbreaks

Jan 9, 2026 | Alignment

Large language models remain vulnerable to jailbreaks—techniques that can circumvent safety guardrails and elicit harmful information. Last year, we described a new approach to defend against jailbreaks which we called "Constitutional Classifiers." The novel aspect was that the classifiers were trained on synthetic data generated from a "constitution."

We have now developed the next generation, Constitutional Classifiers++, described in a new paper. They improve on the previous approach, yielding a system that is even more robust, has a much lower refusal rate, and is dramatically cheaper to run.

## New approaches

We discovered that part of the original system's vulnerability stemmed from the way it evaluated model inputs and outputs separately. We replaced the separate input and output classifiers with a single "exchange" classifier, which monitors outputs in the context of their inputs.

To reduce costs, we implemented a two-stage "cascade architecture." A lightweight first-stage classifier screens all exchanges, and only those it flags proceed to a more accurate second-stage classifier.

We also developed internal probe classifiers that reuse computations already available in the model's neural network. When a model generates text, it produces internal states that capture its understanding. These internal probes are harder to fool and are complementary to our external classifiers.

## Conclusions and further research

Our final production-grade system combines these techniques: a linear probe screens all traffic, escalating flagged exchanges to a probe-classifier ensemble for final judgment. The system achieved a refusal rate of 0.05% on harmless queries—an 87% drop from the original classifiers system. It adds roughly 1% compute overhead.

We conducted over 1,700 cumulative hours of red-teaming across 198,000 attempts. We discovered only one high-risk vulnerability, with no universal jailbreak yet discovered.