---
title: "Building agents with the Claude Agent SDK"
vendor: anthropic
source_url: https://anthropic.com/engineering/building-agents-with-the-claude-agent-sdk
published_at: 2025-09-29T00:00:00.000Z
crawled_at: 2026-05-23T14:36:57.000Z
word_count: 2247
reading_time_minutes: 12
tags: [claude, agent-sdk, ai-agents, development, best-practices]
---

The Claude Agent SDK is a collection of tools that helps developers build powerful agents on top of Claude Code. In this article, we walk through how to get started and share our best practices.

Last year, we shared lessons in building effective agents alongside our customers. Since then, we've released Claude Code, an agentic coding solution that we originally built to support developer productivity at Anthropic.

Over the past several months, Claude Code has become far more than a coding tool. At Anthropic, we've been using it for deep research, video creation, and note-taking, among countless other non-coding applications. In fact, it has begun to power almost all of our major agent loops.

In other words, the agent harness that powers Claude Code (the Claude Code SDK) can power many other types of agents, too. To reflect this broader vision, we're renaming the Claude Code SDK to the Claude Agent SDK.

## Giving Claude a computer

The key design principle behind Claude Code is that Claude needs the same tools that programmers use every day. It needs to be able to find appropriate files in a codebase, write and edit files, lint the code, run it, debug, edit, and sometimes take these actions iteratively until the code succeeds.

By giving Claude access to the user's computer (via the terminal), it had what it needed to write code like programmers do. But this has also made Claude in Claude Code effective at non-coding tasks. By giving it tools to run bash commands, edit files, create files and search files, Claude can read CSV files, search the web, build visualizations, interpret metrics, and do all sorts of other digital work. The key design principle behind the Claude Agent SDK is to give your agents a computer, allowing them to work like humans do.

## Building your agent loop

In Claude Code, Claude often operates in a specific feedback loop: gather context, take action, verify work, repeat. This offers a useful way to think about other agents.

### Gather context
The file system represents information that could be pulled into the model's context. Claude can use bash scripts like grep and tail to load content from logs or user-uploaded files. The Claude Agent SDK supports subagents by default, enabling parallelization and context management.

### Take action
Tools are the primary building blocks of execution for your agent. Bash is useful as a general-purpose tool to allow flexible work using a computer. The SDK excels at code generation—code is precise, composable, and infinitely reusable. MCP (Model Context Protocol) provides standardized integrations to external services.

### Verify your work
Claude Code finishes the agentic loop by evaluating its work. The best form of feedback is providing clearly defined rules for an output. Visual feedback in the form of screenshots or renders can be helpful for UI tasks. You can also have another language model judge the output of your agent.

## Getting started

The Claude Agent SDK makes it easier to build autonomous agents by giving Claude access to a computer where it can write files, run commands, and iterate on its work. With the agent loop in mind, you can build reliable agents that are easy to deploy and iterate on.