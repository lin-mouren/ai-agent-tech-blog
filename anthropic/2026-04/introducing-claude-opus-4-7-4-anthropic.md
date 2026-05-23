---
title: "Introducing Claude Opus 4.7 | Anthropic"
vendor: anthropic
source_url: https://www.anthropic.com/news/claude-opus-4-7
published_at: 2026-04-16T00:00:00.000Z
crawled_at: 2026-05-23T15:34:53.000Z
word_count: 2100
reading_time_minutes: 11
tags: [claude, reasoning, agents, api, product]
---

# Introducing Claude Opus 4.7

Our latest model, Claude Opus 4.7, is now generally available.

Opus 4.7 is a notable improvement on Opus 4.6 in advanced software engineering, with particular gains on the most difficult tasks. Users report being able to hand off their hardest coding work to Opus 4.7 with confidence. Opus 4.7 handles complex, long-running tasks with rigor and consistency, pays precise attention to instructions, and devises ways to verify its own outputs before reporting back.

The model also has substantially better vision: it can see images in greater resolution. It's more tasteful and creative when completing professional tasks, producing higher-quality interfaces, slides, and docs.

## Testing Claude Opus 4.7

Opus 4.7 has garnered strong feedback from early-access testers across many companies, including notable improvements in coding benchmarks, tool use accuracy, and multi-step reasoning. Early testing showed significant improvements in instruction following, multimodal support with higher-resolution images (up to 2,576 pixels on the long edge), and file system-based memory.

## Safety and alignment

Overall, Opus 4.7 shows a similar safety profile to Opus 4.6. On some measures, such as honesty and resistance to malicious prompt injection attacks, Opus 4.7 is an improvement on Opus 4.6. The alignment assessment concluded that the model is "largely well-aligned and trustworthy, though not fully ideal in its behavior."

## Also launching today

Opus 4.7 introduces a new xhigh effort level between high and max, giving users finer control over the tradeoff between reasoning and latency. In Claude Code, we've raised the default effort level to xhigh for all plans. The new /ultrareview command produces a dedicated review session that reads through changes and flags bugs and design issues.

## Migrating from Opus 4.6 to Opus 4.7

Opus 4.7 is a direct upgrade to Opus 4.6. It uses an updated tokenizer, and thinks more at higher effort levels. Users can control token usage via the effort parameter, task budgets, or prompting for conciseness. Opus 4.7 is available across all Claude products and the API at the same pricing as Opus 4.6.
