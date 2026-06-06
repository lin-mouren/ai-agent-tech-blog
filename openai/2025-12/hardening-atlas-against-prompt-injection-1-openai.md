---
title: "Continuously hardening ChatGPT Atlas against prompt injection attacks"
vendor: openai
source_url: https://openai.com/index/hardening-atlas-against-prompt-injection/
published_at: 2025-12-22
tags: [security, prompt-injection, agents, chatgpt-atlas, red-teaming, reinforcement-learning]
---

# Continuously hardening ChatGPT Atlas against prompt injection attacks

**December 22, 2025** | OpenAI

Automated red teaming—powered by reinforcement learning—helps us proactively discover and patch real-world agent exploits before they're weaponized in the wild.

## Overview

Agent mode in ChatGPT Atlas is one of the most general-purpose agentic features OpenAI has released to date. In this mode, the browser agent views webpages and takes actions, clicks, and keystrokes inside your browser, just as you would. This allows ChatGPT to work directly on many day-to-day workflows using the same space, context, and data.

As the browser agent helps you get more done, it also becomes a higher-value target of adversarial attacks. This makes AI security especially important. Long before the launch of ChatGPT Atlas, OpenAI has been continuously building and hardening defenses against emerging threats that specifically target this new "agent in the browser" paradigm. Prompt injection is one of the most significant risks actively defended against to help ensure ChatGPT Atlas can operate securely on your behalf.

## The Prompt Injection Challenge

A prompt injection attack targets AI agents by embedding malicious instructions into content the agent processes. Those instructions are crafted to override or redirect the agent's behavior—hijacking it into following an attacker's intent, rather than the user's.

For a browser agent like the one inside ChatGPT Atlas, prompt injection adds a new threat vector beyond traditional web security risks. Instead of phishing humans or exploiting system vulnerabilities of the browser, the attacker targets the agent operating inside it.

As a hypothetical example, an attacker could send a malicious email attempting to trick an agent to ignore the user's request and instead forward sensitive tax documents to an attacker-controlled email address.

## Automated Attack Discovery via Reinforcement Learning

To strengthen defenses, OpenAI built an LLM-based automated attacker and trained it to hunt for prompt injection attacks. This attacker was trained end-to-end with reinforcement learning, learning from its own successes and failures to improve its red teaming skills.

Key reasons for choosing RL:
1. **Optimizing long-horizon objectives** — adversarial tasks are inherently long-horizon, requiring many steps with sparse and delayed success signals
2. **Leveraging frontier LLM capabilities** — as base models get stronger, the attacker naturally becomes more capable
3. **Scaling compute** — RL scales computation and mimics how adaptive human attackers behave: iteratively trying strategies, learning from outcomes, and reinforcing successful behaviors

## Proactive Rapid Response Loop

OpenAI's automated red teaming drives a proactive rapid response loop:

- **Adversarially training against newly discovered attacks** — continuously training updated agent models against the best automated attacker
- **Using attack traces to improve the broader defense stack** — many attack paths reveal opportunities for improvement in monitoring, safety instructions, or system-level safeguards
- **Responding to active attacks** — attack techniques observed in the wild can be fed into the loop to drive defensive change

## Recommendations for Safe Agent Use

- **Limit logged-in access when possible** — use logged-out mode when access to websites you're logged in to isn't necessary
- **Carefully review confirmation requests** — when an agent asks you to confirm an action, take a moment to verify
- **Give agents explicit instructions** — avoid overly broad prompts like "review my emails and take whatever action is needed"

Prompt injection is viewed as a long-term AI security challenge requiring continuous effort. The goal is for users to be able to trust a ChatGPT agent to use their browser the way they'd trust a highly competent, security-aware colleague or friend.
