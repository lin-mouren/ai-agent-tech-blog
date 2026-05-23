---
title: "Mitigating the risk of prompt injections in browser use"
vendor: anthropic
source_url: https://www.anthropic.com/research/prompt-injection-defenses
published_at: 2025-11-24T00:00:00.000Z
crawled_at: 2026-05-23T14:51:29.000Z
word_count: 1358
reading_time_minutes: 7
tags: [prompt-injection, security, browser-agent, claude, safety]
---

# Mitigating the risk of prompt injections in browser use

Nov 24, 2025

Claude Opus 4.5 sets a new standard in robustness to _prompt injections_—adversarial instructions hidden within the content that AI models process. Our new model is a major improvement over previous ones in both its core performance and in the safeguards surrounding its use. But prompt injection is far from a solved problem, particularly as models take more real-world actions.

## What is prompt injection?

For AI agents to be genuinely useful, they need to be able to act on your behalf—to browse websites, complete tasks, and work with your context and data. But this comes with risk: every webpage an agent visits is a potential vector for attack.

When an agent browses the internet, it encounters content it cannot fully trust. Among legitimate search results, documents, and applications, an attacker might have embedded malicious instructions to hijack the agent and change its behavior. These prompt injection attacks represent one of the most significant security challenges for browser-based AI agents.

## Why browser use creates unique prompt injection risks

Consider a routine task: you ask Claude to read through your recent emails and draft replies to any meeting requests. One of those emails contains hidden instructions embedded in white text, invisible to you but processed by the agent. These instructions direct the agent to forward emails containing the word "confidential" to an external address.

While all agents that process untrusted content are subject to prompt injection risks, browser use amplifies this risk in two ways. First, the attack surface is vast: every webpage, embedded document, advertisement, and dynamically loaded script represents a potential vector. Second, browser agents can take a lot of different actions that attackers can exploit.

## Claude's progress on browser use robustness

Claude Opus 4.5 demonstrates stronger prompt injection robustness in browser use than previous models. Our work has focused on:

**Training Claude to resist prompt injection.** We use reinforcement learning to build prompt injection robustness directly into Claude's capabilities. During model training, we expose Claude to prompt injections embedded in simulated web content, and "reward" it when it correctly identifies and refuses to comply with malicious instructions.

**Improving our classifiers.** We scan all untrusted content that enters the model's context window, and flag potential prompt injections with classifiers. These detect adversarial commands embedded in various forms—hidden text, manipulated images, deceptive UI elements.

**Scaled expert human red teaming.** Human security researchers consistently outperform automated systems at discovering creative attack vectors. Our internal red team continuously probes our browser agent for vulnerabilities.

## The path forward

The web is an adversarial environment, and building browser agents that can operate safely within it requires ongoing vigilance. Prompt injection remains an active area of research, and we are committed to investing in defenses as attack techniques evolve. We will continue to publish our progress transparently.