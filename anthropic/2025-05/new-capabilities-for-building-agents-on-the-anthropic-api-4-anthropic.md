---
title: "New capabilities for building agents on the Anthropic API"
vendor: anthropic
source_url: https://www.anthropic.com/news/agent-capabilities-api/
published_at: 2025-05-22T13:04:58.000Z
crawled_at: 2026-05-23T13:58:13.000Z
word_count: 1000
reading_time_minutes: 5
tags: [api, agents, code-execution, mcp, prompt-caching]
---

# New capabilities for building agents on the Anthropic API

Claude now offers code execution, MCP server connections, file storage, and extended prompt caching through the API—giving developers powerful tools to build agents that analyze data, connect to external systems, and maintain context for longer periods of time.

May 22, 2025

Today, we're announcing four new capabilities on the Anthropic API that enable developers to build more powerful AI agents: the code execution tool, MCP connector, Files API, and the ability to cache prompts for up to one hour.

Together with Claude Opus 4 and Sonnet 4, these beta features enable developers to build agents that execute code for advanced data analysis, connect to external systems through MCP servers, store and access files efficiently across sessions, and maintain context for up to 60 minutes with cost-effective caching.

### Code execution tool

We're introducing a code execution tool on the Anthropic API, giving Claude the ability to run Python code in a sandboxed environment to produce computational results and data visualizations. This transforms Claude from a code-writing assistant into a data analyst that can iterate on visualizations, clean datasets, and derive insights directly within API calls.

Key use cases include financial modeling, scientific computing, business intelligence, document processing, and statistical analysis.

### MCP connector

The MCP connector on the Anthropic API enables developers to connect Claude to any remote Model Context Protocol (MCP) server without writing client code. Previously, connecting to MCP servers required building your own client harness. Now, the Anthropic API handles all connection management, tool discovery, and error handling automatically.

### Files API

The Files API simplifies how developers store and access documents when building with Claude. Instead of managing file uploads in every request, you can now upload documents once and reference them repeatedly across conversations.

### Extended prompt caching

Developers can now choose between our standard 5-minute time to live (TTL) for prompt caching or opt for an extended 1-hour TTL—a 12x improvement that can reduce expenses for long-running agent workflows. With extended caching, customers can reduce costs by up to 90% and latency by up to 85% for long prompts.

### Getting started

All of these features are now available in public beta on the Anthropic API.
