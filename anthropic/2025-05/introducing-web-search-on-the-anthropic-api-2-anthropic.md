---
title: "Introducing web search on the Anthropic API"
vendor: anthropic
source_url: https://www.anthropic.com/news/web-search-api
published_at: 2025-05-07T22:01:07.000Z
crawled_at: 2026-05-23T13:58:13.000Z
word_count: 800
reading_time_minutes: 5
tags: [api, web-search, claude, developers, ai-agents]
---

# Introducing web search on the Anthropic API

Claude can now search the web through the API, giving users access to real-time information with citations for building up-to-date AI applications.

May 7, 2025

Today, we're introducing web search on the Anthropic API—a new tool that gives Claude access to current information from across the web. With web search enabled, developers can build Claude-powered applications and agents that deliver up-to-date insights.

### Power AI agents with the latest information from the web

Developers can now augment Claude's comprehensive knowledge with current, real-world data by enabling the web search tool when making requests to the Messages API.

When Claude receives a request that would benefit from up-to-date information or specialized knowledge, it uses its reasoning capabilities to determine whether the web search tool would help provide a more accurate response. If searching the web would be beneficial, Claude generates a targeted search query, retrieves relevant results, analyzes them for key information, and provides a comprehensive answer with citations back to the source material.

Claude can also operate agentically and conduct multiple progressive searches, using earlier results to inform subsequent queries in order to do light research and generate a more comprehensive answer.

### Use cases

Web search enables Claude to power a wide range of use cases that benefit from real-time data:
- **Financial services:** Build AI agents that analyze real-time stock prices, market trends, and regulatory updates
- **Legal research:** Create tools that access recent court decisions, regulatory changes, and legal news
- **Developer tools:** Enable Claude to reference the latest API documentation, GitHub releases, and technology updates
- **Productivity:** Build agents that incorporate the latest company reports, competitive intelligence, or industry research

### Build with trust and control

Every web-sourced response includes citations to source materials, enabling users to verify information directly. Organizations can maintain additional control through domain allow lists, domain block lists, and organization-level management.

### Getting started

Web search is now available on the Anthropic API for Claude 3.7 Sonnet, the upgraded Claude 3.5 Sonnet, and Claude 3.5 Haiku at $10 per 1,000 searches plus standard token costs.
