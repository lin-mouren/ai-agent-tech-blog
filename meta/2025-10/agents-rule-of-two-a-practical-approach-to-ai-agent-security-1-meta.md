---
title: "Agents Rule of Two: A Practical Approach to AI Agent Security"
vendor: meta
source_url: https://ai.meta.com/blog/practical-ai-agent-security/
published_at: 2025-10-31T00:00:00.000Z
crawled_at: 2026-05-23T14:44:14.000Z
word_count: 1700
reading_time_minutes: 9
tags: [AI-agents, security, prompt-injection, Meta, Llama]
---

October 31, 2025

# Agents Rule of Two: A Practical Approach to AI Agent Security

Imagine a personal AI agent, Email-Bot, that's designed to help you manage your inbox. While the automated email assistant can be of great help, it can also demonstrate how AI agents are introducing novel risks. Notably, one of the biggest challenges is that of agents' susceptibility to prompt injection.

Prompt injection is a fundamental, unsolved weakness in all LLMs. With prompt injection, certain types of untrustworthy strings can cause unintended consequences when passed into an AI agent's context window.

At Meta, we're thinking deeply about how agents can be most useful to people while minimizing bad outcomes from prompt injection. We've developed the Agents Rule of Two.

## Agents Rule of Two

The Agents Rule of Two states that until robustness research allows us to reliably detect and refuse prompt injection, agents must satisfy no more than two of the following three properties within a session:

**[A]** An agent can process untrustworthy inputs
**[B]** An agent can have access to sensitive systems or private data
**[C]** An agent can change state or communicate externally

If an agent requires all three without starting a new session, then the agent should not be permitted to operate autonomously and requires supervision.

## How the Agents Rule of Two Stops Exploitation

Using the Email-Bot example: Prompt injection within a spam email instructs the agent to gather private contents and forward them. This attack requires [A], [B], and [C]. With the Rule of Two, it can be prevented by limiting to [BC] (trustworthy senders only), [AC] (no sensitive data access), or [AB] (no external communication).

## Existing Solutions

Llama Protections offerings include Llama Firewall, Prompt Guard, Code Shield, and Llama Guard for orchestrating agent protections.

## What's Next

The Agents Rule of Two is a useful framework for developers today. As agents become more useful, we'll continue research toward satisfying supervisory approval checks via alignment controls.