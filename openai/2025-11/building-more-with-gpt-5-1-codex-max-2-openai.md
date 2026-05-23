---
title: "Building more with GPT-5.1-Codex-Max"
vendor: openai
source_url: https://www.openai.com/index/gpt-5-1-codex-max/
published_at: 2025-11-19T00:00:00.000Z
crawled_at: 2026-05-23T14:51:29.000Z
word_count: 1637
reading_time_minutes: 9
tags: [codex, gpt-5-1-codex-max, coding-agent, compaction, agentic]
---

Building more with GPT-5.1-Codex-Max | OpenAI

November 19, 2025

[Product](https://openai.com/news/product-releases/) [Release](https://openai.com/research/index/release/)

# Building more with GPT‑5.1‑Codex‑Max

## Introduction

We’re introducing GPT‑5.1‑Codex‑Max, our new frontier agentic coding model, available in Codex today. GPT‑5.1‑Codex‑Max is built on an update to our foundational reasoning model, which is trained on agentic tasks across software engineering, math, research, and more. GPT‑5.1‑Codex‑Max is faster, more intelligent, and more token-efficient at every stage of the development cycle–and a new step towards becoming a reliable coding partner.

GPT‑5.1‑Codex‑Max is built for long-running, detailed work. It’s our first model natively trained to operate across multiple context windows through a process called _compaction_, coherently working over millions of tokens in a single task. This unlocks project-scale refactors, deep debugging sessions, and multi-hour agent loops.

GPT‑5.1‑Codex‑Max is available in Codex today for use in the CLI, IDE extension, cloud, and code review, and API access is coming soon.

## Frontier coding capabilities

GPT‑5.1‑Codex‑Max was trained on real-world software engineering tasks, like PR creation, code review, frontend coding, and Q&A and outperforms our previous models on many frontier coding evaluations. The model's gains on benchmarks also come with improvements to real-world usage: GPT‑5.1‑Codex‑Max is the first model we have trained to operate in Windows environments, and the model's training now includes tasks designed to make it a better collaborator in the Codex CLI.

On SWE-Lancer IC SWE, GPT‑5.1‑Codex-Max achieved 79.9% vs 66.3% for GPT‑5.1‑Codex. On Terminal-Bench 2.0 it scored 58.1% vs 52.8%.

## Speed and cost

GPT‑5.1‑Codex‑Max shows significant improvements in token efficiency due to more effective reasoning. On SWE-bench Verified, GPT‑5.1‑Codex‑Max with 'medium' reasoning effort outperforms GPT‑5.1‑Codex at the same setting while using 30% fewer thinking tokens.

## Long-running tasks

Compaction enables GPT‑5.1‑Codex‑Max to complete tasks that would have previously failed due to context-window limits. The model can work independently for hours at a time. In internal evaluations, we've observed GPT‑5.1‑Codex‑Max work on tasks for more than 24 hours, persistently iterating on implementations, fixing test failures, and delivering successful results.

## Building safe and trustworthy AI agents

GPT‑5.1‑Codex‑Max performs significantly better on evaluations requiring sustained, long-horizon reasoning. It does not reach High capability on Cybersecurity under our Preparedness Framework but is the most capable cybersecurity model we've deployed to date.

Codex is designed to run in a secure sandbox by default: file writes are limited to its workspace, and network access is disabled unless a developer turns it on.

## Availability

GPT‑5.1‑Codex‑Max is available in Codex with ChatGPT Plus, Pro, Business, Edu, and Enterprise plans. Starting today, GPT‑5.1‑Codex‑Max will replace GPT‑5.1‑Codex as the default model in Codex surfaces.

## Conclusion

GPT‑5.1‑Codex‑Max shows how far models have come in sustaining long-horizon coding tasks. Internally, 95% of OpenAI engineers use Codex weekly, and these engineers ship roughly 70% more pull requests since adopting Codex.