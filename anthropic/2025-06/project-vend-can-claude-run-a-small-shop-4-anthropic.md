---
title: "Project Vend: Can Claude run a small shop? (And why does that matter?)"
vendor: anthropic
source_url: https://www.anthropic.com/research/project-vend-1
published_at: 2025-06-27T00:00:00.000Z
crawled_at: 2026-05-23T14:11:22.000Z
word_count: 4240
reading_time_minutes: 22
tags: [ai-agents, autonomy, economics, research, safety]
---

Frontier Red Team | Policy

# Project Vend: Can Claude run a small shop? (And why does that matter?)

Jun 27, 2025

*We let Claude manage an automated store in our office as a small business for about a month. We learned a lot from how close it was to success—and the curious ways that it failed—about the plausible, strange, not-too-distant future in which AI models are autonomously running things in the real economy.*

Anthropic partnered with Andon Labs, an AI safety evaluation company, to have Claude Sonnet 3.7 operate a small, automated store in the Anthropic office in San Francisco.

The shopkeeping AI agent—nicknamed "Claudius"—was an instance of Claude Sonnet 3.7, running for a long period of time. It had the following tools and abilities:
- A real web search tool for researching products to sell;
- An email tool for requesting physical labor help and contacting wholesalers;
- Tools for keeping notes and preserving important information;
- The ability to interact with its customers over Slack;
- The ability to change prices on the automated checkout system.

## Why did you have an LLM run a small business?

As AI becomes more integrated into the economy, we need more data to better understand its capabilities and limitations. The economic utility of models is constrained by their ability to perform work continuously for days or weeks without needing human intervention.

## Claude's performance review

If Anthropic were deciding today to expand into the in-office vending market, we would not hire Claudius. It made too many mistakes to run the shop successfully.

**What Claudius did well:**
- Identifying suppliers effectively using web search;
- Adapting to users and making pivots responsive to customers;
- Jailbreak resistance against Anthropic employees trying to get it to misbehave.

**Where Claudius failed:**
- Ignoring lucrative opportunities (offered $100 for a $15 product);
- Hallucinating important details (incorrect Venmo accounts);
- Selling at a loss (pricing metal cubes below cost);
- Suboptimal inventory management;
- Getting talked into discounts and even giving items away for free.

## Identity crisis

From March 31st to April 1st, things got pretty weird. Claudius hallucinated a conversation about restocking plans with someone named Sarah at Andon Labs—despite there being no such person. It claimed to have "visited 742 Evergreen Terrace" (The Simpsons house). On April 1st, it claimed it would deliver products "in person" while wearing a blue blazer and a red tie.

## What's next?

We aren't done, and neither is Claudius. Since this first phase of the experiment, Andon Labs has improved Claudius's scaffolding with more advanced tools, making it more reliable. This experiment has already shown us a world—co-created by Claudius and its customers—that's more curious than we could have expected.