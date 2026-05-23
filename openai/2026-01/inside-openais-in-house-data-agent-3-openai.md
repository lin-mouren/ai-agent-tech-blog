---
title: "Inside OpenAI's in-house data agent"
vendor: openai
source_url: https://openai.com/index/inside-our-in-house-data-agent/
published_at: 2026-01-29T00:00:00.000Z
crawled_at: 2026-05-23T15:06:50.000Z
word_count: 3000
reading_time_minutes: 15
tags: [data-agent, internal-tools, gpt-5, rag, memory]
---

# Inside OpenAI's in-house data agent

January 29, 2026 | Engineering

By Bonnie Xu, Aravind Suresh, and Emma Tang

Data powers how systems learn, products evolve, and how companies make choices. But getting answers quickly, correctly, and with the right context is often harder than it should be. To make this easier as OpenAI scales, we built our own bespoke in-house AI data agent that explores and reasons over our own platform.

Our agent is a custom internal-only tool, built specifically around OpenAI's data, permissions, and workflows. We are showing how we built and use it to help surface examples of the real, impactful ways AI can support day-to-day work across our teams. The OpenAI tools we used to build and run it (Codex, our GPT-5 flagship model, the Evals API, and the Embeddings API) are the same tools we make available to developers everywhere.

Our data agent lets employees go from question to insight in minutes, not days. This lowers the bar to pulling data and nuanced analysis across all functions, not just by our data team. Today, teams across Engineering, Data Science, Go-To-Market, Finance, and Research at OpenAI lean on the agent to answer high-impact data questions.

## Why we needed a custom tool

OpenAI's data platform serves more than 3.5k internal users working across Engineering, Product, and Research, spanning over 600 petabytes of data across 70k datasets. At that size, simply finding the right table can be one of the most time-consuming parts of doing analysis.

Even with the correct tables selected, producing correct results can be challenging. Analysts must reason about table data and table relationships to ensure transformations and filters are applied correctly. Common failure modes—many-to-many joins, filter pushdown errors, and unhandled nulls—can silently invalidate results.

## How it works

Our agent is powered by GPT-5.2 and is designed to reason over OpenAI's data platform. It is available wherever employees already work: as a Slack agent, through a web interface, inside IDEs, in the Codex CLI via MCP, and directly in OpenAI's internal ChatGPT app through an MCP connector.

Users can ask complex, open-ended questions which would typically require multiple rounds of manual exploration. The agent handles the analysis end-to-end, from understanding the question to exploring the data, running queries, and synthesizing findings.

One of the agent's superpowers is how it reasons through problems. Rather than following a fixed script, the agent evaluates its own progress. If an intermediate result looks wrong, the agent investigates what went wrong, adjusts its approach, and tries again.

## Context is everything

High-quality answers depend on rich, accurate context. The agent is built around multiple layers of context that ground it in OpenAI's data and institutional knowledge:

1. **Table Usage** - Schema metadata, column names, data types
2. **Human Annotations** - Curated descriptions by domain experts
3. **Codex Enrichment** - Code-level understanding of table meaning
4. **Institutional Knowledge** - Access to Slack, Google Docs, and Notion
5. **Memory** - Learns from corrections and discoveries
6. **Runtime Context** - Live queries to validate schemas

## Lessons learned

- **Less is More**: Early on, we exposed our full tool set and ran into problems with overlapping functionality. We restricted and consolidated certain tool calls.
- **Guide the Goal, Not the Path**: Highly prescriptive prompting degraded results. Shifting to higher-level guidance improved results.
- **Meaning Lives in Code**: Schemas describe a table's shape, but its true meaning lives in the code that produces it.