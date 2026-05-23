---
title: "Speeding up agentic workflows with WebSockets in the Responses API | OpenAI"
vendor: openai
source_url: https://openai.com/index/speeding-up-agentic-workflows-with-websockets/
published_at: 2026-04-22T00:00:00.000Z
crawled_at: 2026-05-23T15:34:53.000Z
word_count: 1950
reading_time_minutes: 10
tags: [api, agents, engineering, codex, infrastructure]
---

# Speeding up agentic workflows with WebSockets in the Responses API

By Brian Yu and Ashwin Nathan, Members of the Technical Staff

When you ask Codex to fix a bug, it scans through your codebase for relevant files, reads them to build context, makes edits, and runs tests to verify the fix worked. Under the hood, that means dozens of back-and-forth Responses API requests. All of these requests can add up to minutes that users spend waiting for Codex to complete complex tasks.

In this post, we'll explain how we made agent loops using the API 40% faster end-to-end, letting users experience the jump in inference speed from 65 to nearly 1,000 tokens per second.

## When the API became the bottleneck

In the Responses API, previous flagship models like GPT-5 and GPT-5.2 ran at roughly 65 tokens per second. For the launch of GPT-5.3-Codex-Spark, a fast coding model, our goal was over 1,000 TPS. To make sure users could experience the true speed of this new model, we had to reduce API overhead.

Around November 2025, we launched a performance sprint on the Responses API, landing many optimizations:
- Caching rendered tokens and model configuration in memory
- Reducing network hop latency by eliminating calls to intermediate services
- Improving our safety stack so we could run certain classifiers faster

With these improvements, we saw close to a 45% improvement in time to first token (TTFT), but these improvements were still not fast enough for GPT-5.3-Codex-Spark.

## Building a persistent connection

We landed on WebSockets because as a simple message transport protocol, users wouldn't have to change their Responses API input and output shapes. On a WebSocket connection, the server keeps a connection-scoped, in-memory cache of previous response state. When a follow-up response.create includes previous_response_id, we fetch that state from the cache instead of rebuilding the full conversation from scratch.

## Setting a new bar for speed

Alpha users reported up to 40% improvements in their agentic workflows. The launch results were immediate:
- Codex quickly ramped up the majority of their Responses API traffic onto WebSocket mode
- For GPT-5.3-Codex-Spark, we hit our 1,000 TPS target and saw bursts up to 4,000 TPS
- Vercel integrated WebSocket mode into the AI SDK and saw latency decrease by up to 40%
- Cline's multi-file workflows are 39% faster
- OpenAI models in Cursor became up to 30% faster

WebSocket mode is one of the most significant new capabilities in the Responses API since its launch in March 2025. It not only dramatically improves agent rollout latency but also supports a growing need: as model inference gets faster, the services and systems that surround inference also need to speed up.
