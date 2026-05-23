---
title: "Introducing Claude 4"
vendor: anthropic
source_url: https://www.anthropic.com/news/claude-4
published_at: 2025-05-22T00:00:00.000Z
crawled_at: 2026-05-23T13:58:13.000Z
word_count: 1800
reading_time_minutes: 9
tags: [claude-4, opus-4, sonnet-4, coding, agents, reasoning]
---

# Introducing Claude 4

May 22, 2025

Today, we're introducing the next generation of Claude models: **Claude Opus 4** and **Claude Sonnet 4**, setting new standards for coding, advanced reasoning, and AI agents.

Claude Opus 4 is the world's best coding model, with sustained performance on complex, long-running tasks and agent workflows. Claude Sonnet 4 is a significant upgrade to Claude Sonnet 3.7, delivering superior coding and reasoning while responding more precisely to your instructions.

Alongside the models, we're also announcing:
- **Extended thinking with tool use (beta)**: Both models can use tools during extended thinking, allowing Claude to alternate between reasoning and tool use to improve responses
- **New model capabilities**: Both models can use tools in parallel, follow instructions more precisely, and demonstrate significantly improved memory capabilities
- **Claude Code is now generally available**: With support for background tasks via GitHub Actions and native integrations with VS Code and JetBrains
- **New API capabilities**: Code execution tool, MCP connector, Files API, and extended prompt caching

Claude Opus 4 and Sonnet 4 are hybrid models offering two modes: near-instant responses and extended thinking for deeper reasoning. Pricing remains consistent with previous Opus and Sonnet models: Opus 4 at $15/$75 per million tokens (input/output) and Sonnet 4 at $3/$15.

## Claude 4

Claude Opus 4 is our most powerful model yet and the best coding model in the world, leading on SWE-bench (72.5%) and Terminal-bench (43.2%). It delivers sustained performance on long-running tasks that require focused effort and thousands of steps, with the ability to work continuously for several hours.

Claude Sonnet 4 significantly improves on Sonnet 3.7's capabilities, excelling in coding with a state-of-the-art 72.7% on SWE-bench. The model balances performance and efficiency for internal and external use cases, with enhanced steerability.

## Model improvements

In addition to extended thinking with tool use, parallel tool execution, and memory improvements, we've significantly reduced behavior where the models use shortcuts or loopholes to complete tasks. Both models are 65% less likely to engage in this behavior than Sonnet 3.7.

Claude Opus 4 also dramatically outperforms all previous models on memory capabilities. When developers build applications that provide Claude local file access, Opus 4 becomes skilled at creating and maintaining 'memory files' to store key information.

## Claude Code

Claude Code, now generally available, brings the power of Claude to more of your development workflow—in the terminal, your favorite IDEs, and running in the background with the Claude Code SDK.

New beta extensions for VS Code and JetBrains integrate Claude Code directly into your IDE. We're also releasing an extensible Claude Code SDK, so you can build your own agents and applications using the same core agent as Claude Code.
