---
title: "Making Claude Code more secure and autonomous with sandboxing"
vendor: anthropic
source_url: https://www.anthropic.com/engineering/claude-code-sandboxing
published_at: 2025-10-20T00:00:00.000Z
crawled_at: 2026-05-23T14:44:14.000Z
word_count: 1300
reading_time_minutes: 7
tags: [claude-code, sandboxing, security, AI-agents, Anthropic]
---

Published Oct 20, 2025

# Beyond permission prompts: making Claude Code more secure and autonomous

Claude Code's new sandboxing features reduce permission prompts and increase user safety by enabling two boundaries: filesystem and network isolation.

## Keeping users secure on Claude Code

Claude Code runs on a permission-based model. To address approval fatigue, we introduced sandboxing for Claude Code.

## Sandboxing: a safer and more autonomous approach

Sandboxing creates pre-defined boundaries within which Claude can work more freely. Our approach enables two boundaries:

1. **Filesystem isolation**: ensures Claude can only access or modify specific directories, preventing prompt-injected Claude from modifying sensitive system files.
2. **Network isolation**: ensures Claude can only connect to approved servers, preventing data exfiltration or malware downloads.

Effective sandboxing requires both filesystem and network isolation.

### Sandboxed bash tool

We're introducing a new sandbox runtime, available in beta, that lets you define exactly which directories and network hosts your agent can access. In Claude Code, we use this runtime to sandbox the bash tool, allowing Claude to run commands within defined limits.

We've built this on top of OS level primitives such as Linux bubblewrap and MacOS seatbelt. Sandboxing ensures that even a successful prompt injection is fully isolated.

### Claude Code on the web

Claude Code on the web executes each session in an isolated sandbox where sensitive credentials are never inside the sandbox. Claude Code on the web uses a custom proxy service that transparently handles all git interactions.

## Getting started

To get started, run `/sandbox` in Claude Code and check out the docs on how to configure this sandbox. The sandbox runtime is also available as an open source research preview.