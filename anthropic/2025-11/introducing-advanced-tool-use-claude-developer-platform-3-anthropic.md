---
title: "Introducing advanced tool use on the Claude Developer Platform"
vendor: anthropic
source_url: https://www.anthropic.com/engineering/advanced-tool-use
published_at: 2025-11-24T00:00:00.000Z
crawled_at: 2026-05-23T14:51:29.000Z
word_count: 5781
reading_time_minutes: 29
tags: [claude, tool-use, programmatic-tool-calling, mcp, agents]
---

# Introducing advanced tool use on the Claude Developer Platform

Published Nov 24, 2025

We've added three new beta features that let Claude discover, learn, and execute tools dynamically. Here's how they work.

The future of AI agents is one where models work seamlessly across hundreds or thousands of tools. An IDE assistant that integrates git operations, file manipulation, package managers, testing frameworks, and deployment pipelines. An operations coordinator that connects Slack, GitHub, Google Drive, Jira, company databases, and dozens of MCP servers simultaneously.

To build effective agents, they need to work with unlimited tool libraries without stuffing every definition into context upfront. Agents should discover and load tools on-demand, keeping only what's relevant for the current task.

Today, we're releasing three features:

- **Tool Search Tool,** which allows Claude to use search tools to access thousands of tools without consuming its context window
- **Programmatic Tool Calling**, which allows Claude to invoke tools in a code execution environment reducing the impact on the model's context window
- **Tool Use Examples**, which provides a universal standard for demonstrating how to effectively use a given tool

## Tool Search Tool

Instead of loading all tool definitions upfront, the Tool Search Tool discovers tools on-demand. Claude only sees the tools it actually needs for the current task.

Consider a five-server MCP setup: GitHub (35 tools, ~26K tokens), Slack (11 tools, ~21K tokens), Sentry (5 tools, ~3K tokens), Grafana (5 tools, ~3K tokens), Splunk (2 tools, ~2K tokens). That's 58 tools consuming ~55K tokens before any conversation starts.

With the Tool Search Tool: only the search tool loaded upfront (~500 tokens), tools discovered on-demand (3-5 relevant tools, ~3K tokens). Total: ~8.7K tokens, preserving 95% of context window. An 85% reduction in token usage.

Internal testing showed significant accuracy improvements: Opus 4 improved from 49% to 74%, and Opus 4.5 improved from 79.5% to 88.1% with Tool Search Tool enabled.

## Programmatic Tool Calling

Programmatic Tool Calling enables Claude to orchestrate tools through code rather than through individual API round-trips. Instead of Claude requesting tools one at a time, Claude writes code that calls multiple tools, processes their outputs, and controls what information actually enters its context window.

Key benefits:
- **Token savings**: Average usage dropped from 43,588 to 27,297 tokens (37% reduction)
- **Reduced latency**: When Claude orchestrates 20+ tool calls in a single code block, you eliminate 19+ inference passes
- **Improved accuracy**: Knowledge retrieval improved from 25.6% to 28.5%

## Tool Use Examples

Tool Use Examples let you provide sample tool calls directly in your tool definitions. Instead of relying on schema alone, you show Claude concrete usage patterns.

Internal testing showed tool use examples improved accuracy from 72% to 90% on complex parameter handling.

## Getting started

These features are available in beta. To enable them, add the beta header `advanced-tool-use-2025-11-20` and include the tools you need. These features move tool use from simple function calling toward intelligent orchestration.