---
title: "Unrolling the Codex agent loop"
vendor: openai
source_url: https://openai.com/index/unrolling-the-codex-agent-loop/
published_at: 2026-01-23T00:00:00.000Z
crawled_at: 2026-05-23T15:06:50.000Z
word_count: 3500
reading_time_minutes: 18
tags: [codex, agent-loop, responses-api, prompt-caching, engineering]
---

# Unrolling the Codex agent loop

January 23, 2026 | Engineering

By Michael Bolin, Member of the Technical Staff

Codex CLI is our cross-platform local software agent, designed to produce high-quality, reliable software changes while operating safely and efficiently on your machine. We have learned a tremendous amount about how to build a world-class software agent since we first launched the CLI in April. To unpack those insights, this is the first post in an ongoing series where we will explore various aspects of how Codex works, as well as hard-earned lessons.

To kick off, we will focus on the agent loop, which is the core logic in Codex CLI that is responsible for orchestrating the interaction between the user, the model, and the tools the model invokes to perform meaningful software work.

## The agent loop

At the heart of every AI agent is something called "the agent loop." To start, the agent takes input from the user to include in the set of textual instructions it prepares for the model known as a prompt. The next step is to query the model by sending it our instructions and asking it to generate a response, a process known as inference.

As the result of the inference step, the model either produces a final response to the user's original input, or requests a tool call that the agent is expected to perform. In the case of a tool call, the agent executes the tool call and appends its output to the original prompt. This process repeats until the model stops emitting tool calls and instead produces a message for the user.

## Model inference

The Codex CLI sends HTTP requests to the Responses API to run model inference. The Responses API endpoint that the Codex CLI uses is configurable, so it can be used with any endpoint that implements the Responses API.

### Building the initial prompt
The prompt is built from multiple components: instructions, tools, and input. Codex inserts system messages about the sandbox, developer instructions, user instructions from AGENTS.md files, and environment context.

### Performance considerations
The agent loop can be quadratic in terms of JSON sent to the Responses API. To mitigate this, Codex relies on prompt caching, which enables reuse of computation from previous inference calls. The Codex team must be diligent when introducing new features that could compromise prompt caching.

### Context window management
The general strategy to avoid running out of context window is to compact the conversation once the number of tokens exceeds some threshold. The Responses API supports a /responses/compact endpoint that performs compaction efficiently.