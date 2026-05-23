---
title: "Partnering with Mozilla to improve Firefox's security | Anthropic"
vendor: anthropic
source_url: https://red.anthropic.com/2026/firefox/
published_at: 2026-03-06T00:00:00.000Z
crawled_at: 2026-05-23T15:30:04.000Z
word_count: 1650
reading_time_minutes: 9
tags: [claude, safety, research, agents, security]
---

# Partnering with Mozilla to improve Firefox's security

March 6, 2026

AI models can now independently identify high-severity vulnerabilities in complex software. As we recently documented, Claude found more than 500 zero-day vulnerabilities in well-tested open-source software.

In this post, we share details of a collaboration with researchers at Mozilla in which Claude Opus 4.6 discovered 22 vulnerabilities over the course of two weeks. Of these, Mozilla assigned 14 as high-severity vulnerabilities - almost a fifth of all high-severity Firefox vulnerabilities that were remediated in 2025.

## From model evaluations to a security partnership

We chose Firefox because it is both a complex codebase and one of the most well-tested and secure open-source projects in the world. After just twenty minutes of exploration, Claude Opus 4.6 reported that it had identified a Use After Free vulnerability in the JavaScript engine. By the end of this effort, we had scanned nearly 6,000 C++ files and submitted a total of 112 unique reports.

## From identifying vulnerabilities to writing primitive exploits

To measure the upper limits of Claude's cybersecurity abilities, we tested whether Claude could exploit the bugs it discovered. We ran this test several hundred times with different starting points, spending approximately $4,000 in API credits. Opus 4.6 was only able to turn a vulnerability into an exploit in two cases - Claude is much better at finding bugs than exploiting them.

## What is next for AI-enabled cybersecurity

These early signs of AI-enabled exploit development underscore the importance of accelerating the find-and-fix process for defenders. In our experience, Claude works best when it is able to check its own work with another tool, which we call a "task verifier": a trusted method of confirming whether an AI agent's output achieves its goal.

Frontier language models are now world-class vulnerability researchers. Opus 4.6 is currently far better at identifying and fixing vulnerabilities than at exploiting them, giving defenders the advantage.