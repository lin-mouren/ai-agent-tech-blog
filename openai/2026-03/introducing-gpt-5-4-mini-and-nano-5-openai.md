---
title: "Introducing GPT-5.4 mini and nano | OpenAI"
vendor: openai
source_url: https://openai.com/index/introducing-gpt-5-4-mini-and-nano/
published_at: 2026-03-17T00:00:00.000Z
crawled_at: 2026-05-23T15:30:04.000Z
word_count: 968
reading_time_minutes: 5
tags: [gpt, reasoning, agents, api, product]
---

OpenAI

March 17, 2026

[Company](https://openai.com/news/company-announcements/) [Product](https://openai.com/news/product-releases/)

# Introducing GPT-5.4 mini and nano

Fast and efficient models optimized for coding and subagents

Loading...

Share

Today we're releasing GPT-5.4 mini and nano, our most capable small models yet. They bring many of the strengths of GPT-5.4 to faster, more efficient models designed for high-volume workloads.

GPT-5.4 mini significantly improves over GPT-5 mini across coding, reasoning, multimodal understanding, and tool use, while running more than 2x faster. It also approaches the performance of the larger GPT-5.4 model on several evaluations, including SWE-Bench Pro and OSWorld-Verified.

GPT-5.4 nano is the smallest, cheapest version of GPT-5.4 for tasks where speed and cost matter most. It is also a significant upgrade over GPT-5 nano. We recommend it for classification, data extraction, ranking, and coding subagents that handle simpler supporting tasks.

These models are built for the kinds of workloads where latency directly shapes the product experience: coding assistants that need to feel responsive, subagents that quickly complete supporting tasks, computer-using systems that capture and interpret screenshots, and multimodal applications that can reason over images in real-time.

In benchmarks, GPT-5.4 mini consistently outperforms GPT-5-mini at similar latencies and approaches GPT-5.4-level pass rates while running much faster.

GPT-5.4 mini is also a strong fit for systems that combine models of different sizes. In Codex, for example, a larger model like GPT-5.4 can handle planning, coordination, and final judgment, while delegating to GPT-5.4 mini subagents that handle narrower subtasks in parallel.

GPT-5.4 mini is available today in the API, Codex, and ChatGPT. In the API, it supports text and image inputs, tool use, function calling, web search, file search, computer use, and skills. It has a 400k context window and costs $0.75 per 1M input tokens and $4.50 per 1M output tokens. GPT-5.4 nano is only available in the API and costs $0.20 per 1M input tokens and $1.25 per 1M output tokens.

Key evaluation results: GPT-5.4 mini achieves 54.4% on SWE-Bench Pro, 72.1% on OSWorld-Verified, 88.0% on GPQA Diamond, and 42.9% on Toolathlon at xhigh reasoning effort, approaching the performance of the full GPT-5.4 model at fraction of the cost.