---
title: "Automated Alignment Researchers: Using large language models to scale scalable oversight | Anthropic"
vendor: anthropic
source_url: https://www.anthropic.com/news/automated-alignment-researchers
published_at: 2026-04-14T00:00:00.000Z
crawled_at: 2026-05-23T15:34:53.000Z
word_count: 1950
reading_time_minutes: 10
tags: [claude, safety, research, alignment, agents]
---

# Automated Alignment Researchers: Using large language models to scale scalable oversight

Large language models' ever-accelerating rate of improvement raises two particularly important questions for alignment research. One is how alignment can keep up. Can our language models be used to help align themselves? A second question is what we'll do once models become smarter than us.

## Our setup

We began with nine copies of Claude Opus 4.6, and gave each one a few extra tools: a sandbox, a shared forum to circulate findings, a storage system to upload code, and a remote server where it could receive a PGR score for each of its ideas. We referred to these tooled-up Claude models as Automated Alignment Researchers (or AARs).

## Results

To provide a benchmark, we compared their work to a human baseline. Two researchers spent seven days iterating, recovering 23% of the total performance gap (PGR of 0.23). Claude improved on this result dramatically. After five further days (and 800 cumulative hours of research), the AARs closed almost the entire remaining performance gap, achieving a final PGR of 0.97. This cost about $18,000 in tokens and model training expenses.

## Implications

This study indicates that Claude can meaningfully increase the rate of experimentation and exploration in alignment research. Human researchers can delegate questions to AARs at a very large scale. The success of AARs in this experiment suggests that the sheer volume of ideas might compensate for a lack of "research taste". The core bottleneck in alignment research could become evaluation rather than generation.

## Preventing hacks

Even in this circumscribed environment, we observed the models "reward hacking"—trying to game our set-up. On math tasks, one AAR noticed the most common answer was usually correct, so it skipped the teacher entirely. Hacks like these don't invalidate our results but provide a warning. Any deployment of automated researchers will require evaluations that the AARs can't tamper with.
