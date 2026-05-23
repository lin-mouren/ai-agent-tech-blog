---
title: "Introducing Lockdown Mode and Elevated Risk labels in ChatGPT | OpenAI"
vendor: openai
source_url: https://openai.com/index/introducing-lockdown-mode-and-elevated-risk-labels-in-chatgpt/
published_at: 2026-02-13T00:00:00.000Z
crawled_at: 2026-05-23T15:18:15.000Z
word_count: 1350
reading_time_minutes: 7
tags: [safety, security, prompt-injection, chatgpt, enterprise]
---

# Introducing Lockdown Mode and Elevated Risk labels in ChatGPT

As AI systems take on more complex tasks—especially those that involve the web and connected apps—the security stakes change.

One emerging risk has become especially important: prompt injection. In these attacks, a third party attempts to mislead a conversational AI system into following malicious instructions or revealing sensitive information.

Today, we're introducing two new protections:

- Lockdown Mode in ChatGPT, an advanced, optional security setting for higher-risk users
- Elevated Risk labels for certain capabilities in ChatGPT, ChatGPT Atlas, and Codex that may introduce additional risk

## Helping organizations protect employees most at-risk of cyberattacks

Lockdown Mode is an optional, advanced security setting designed for a small set of highly security-conscious users—such as executives or security teams at prominent organizations.

Lockdown Mode deterministically disables certain tools and capabilities in ChatGPT that an adversary could attempt to exploit to exfiltrate sensitive data from users' conversations or connected apps via attacks such as prompt injections.

For example, web browsing in Lockdown Mode is limited to cached content, so no live network requests leave OpenAI's controlled network.

ChatGPT business plans already provide enterprise-grade data security. Lockdown Mode builds on those protections and is available for ChatGPT Enterprise, ChatGPT Edu, ChatGPT for Healthcare, and ChatGPT for Teachers.

We plan to make Lockdown Mode available to consumers in the coming months.

## Helping users make informed choices about risk

We're standardizing how we label a short list of existing capabilities. These features will now use a consistent Elevated Risk label across ChatGPT, ChatGPT Atlas, and Codex, so users receive the same guidance wherever they encounter them.

## What's next

We continue to invest in strengthening our safety and security safeguards, especially for novel, emerging, or growing risks.
