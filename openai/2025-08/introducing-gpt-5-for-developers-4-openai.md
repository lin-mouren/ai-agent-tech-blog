---
title: "Introducing GPT-5 for developers | OpenAI"
vendor: openai
source_url: https://openai.com/index/introducing-gpt-5-for-developers/
published_at: 2025-08-07T00:00:00.000Z
crawled_at: 2026-05-23T14:29:11.000Z
word_count: 2580
reading_time_minutes: 13
tags: [gpt, api, coding, agents, reasoning]
---

# Introducing GPT-5 for developers

August 7, 2025

The best model for coding and agentic tasks.

## Introduction

Today, we're releasing GPT-5 in our API platform—our best model yet for coding and agentic tasks.

GPT-5 is state-of-the-art across key coding benchmarks, scoring 74.9% on SWE-bench Verified and 88% on Aider polyglot. We trained GPT-5 to be a true coding collaborator. It excels at producing high-quality code and handling tasks such as fixing bugs, editing code, and answering questions about complex codebases.

We trained GPT-5 on real-world coding tasks in collaboration with early testers across startups and enterprises. Cursor says GPT-5 is "the smartest model they've used." Windsurf shared GPT-5 is SOTA on their evals and "has half the tool calling error rate over other frontier models."

GPT-5 also excels at long-running agentic tasks—achieving SOTA results on tau2-bench telecom (96.7%). GPT-5's improved tool intelligence lets it reliably chain together dozens of tool calls without losing its way.

## New features

### Minimal reasoning effort
Developers can control GPT-5's thinking time via the reasoning_effort parameter in the API, now supporting minimal, low, medium, and high values.

### Verbosity
A new API parameter verbosity takes values of low, medium, and high to steer response length.

### Custom tools
A new tool type that allows GPT-5 to call a tool with plaintext instead of JSON, with support for regex and context-free grammar constraints.

## Availability & pricing

GPT-5 is available now in the API platform in three sizes: gpt-5, gpt-5-mini, and gpt-5-nano. GPT-5 is priced at $1.25/1M input tokens and $10/1M output tokens.
