---
title: "Keeping your data safe when an AI agent clicks a link"
vendor: openai
source_url: https://openai.com/index/ai-agent-link-safety/
published_at: 2026-01-28T00:00:00.000Z
crawled_at: 2026-05-23T15:06:50.000Z
word_count: 1500
reading_time_minutes: 8
tags: [agent-safety, prompt-injection, data-exfiltration, security, privacy]
---

# Keeping your data safe when an AI agent clicks a link

January 28, 2026 | Safety | Security

By Adrian Spânu, Thomas Shadwell

AI systems are getting better at taking actions on your behalf, opening a web page, following a link, or loading an image to help answer a question. These useful capabilities also introduce subtle risks that we work tirelessly to mitigate.

This post explains one specific class of attacks we defend against: URL-based data exfiltration, and how we have built safeguards to reduce the risk when ChatGPT (and agentic experiences) retrieve web content.

## The problem: a URL can carry more than a destination

When you click a link in your browser, you are not just going to a website, you are also sending the website the URL you requested. Websites commonly log requested URLs in analytics and server logs.

Normally, that is fine. But an attacker can try to trick a model into requesting a URL that secretly contains sensitive information, like an email address, a document title, or other data the AI might have access to while helping you.

This is especially relevant because attackers can use prompt injection techniques: they place instructions in web content that try to override what the model should do.

## Our approach: allow automatic fetching only for URLs that are already public

To reduce the chance that a URL contains user-specific secrets, we use a simple principle: If a URL is already known to exist publicly on the web, independently of any user's conversation, then it is much less likely to contain that user's private data.

To operationalize that, we rely on an independent web index (a crawler) that discovers and records public URLs without any access to user conversations, accounts, or personal data.

Then, when an agent is about to retrieve a URL automatically, we check whether that URL matches a URL previously observed by the independent index.

- If it matches: the agent can load it automatically
- If it does not match: we treat it as unverified and require explicit user action

## What this protects against and what it does not

These safeguards are aimed at preventing the agent from quietly leaking user-specific data through the URL itself when fetching resources. It does not automatically guarantee that the content of a web page is trustworthy, or that a site will not try to socially engineer you.

We treat this as one layer in a broader, defense-in-depth strategy that includes model-level mitigations against prompt injection, product controls, monitoring, and ongoing red-teaming.