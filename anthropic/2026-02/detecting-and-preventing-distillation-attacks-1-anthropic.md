---
title: "Detecting and preventing distillation attacks"
vendor: anthropic
source_url: https://www.anthropic.com/research/detecting-and-preventing-distillation-attacks
published_at: 2026-02-23T00:00:00.000Z
crawled_at: 2026-05-23T15:18:15.000Z
word_count: 2150
reading_time_minutes: 11
tags: [security, distillation, anthropic, ai-safety, china]
---

# Detecting and preventing distillation attacks

We have identified industrial-scale campaigns by three AI laboratories—DeepSeek, Moonshot, and MiniMax—to illicitly extract Claude's capabilities to improve their own models. These labs generated over 16 million exchanges with Claude through approximately 24,000 fraudulent accounts, in violation of our terms of service and regional access restrictions.

These labs used a technique called distillation, which involves training a less capable model on the outputs of a stronger one. Distillation is a widely used and legitimate training method, but can also be used for illicit purposes.

## Why distillation matters

Illicitly distilled models lack necessary safeguards, creating significant national security risks. Foreign labs that distill American models can feed these unprotected capabilities into military, intelligence, and surveillance systems.

## What we found

The three distillation campaigns followed a similar playbook, using fraudulent accounts and proxy services to access Claude at scale while evading detection.

### DeepSeek
Scale: Over 150,000 exchanges. Targeted reasoning capabilities, rubric-based grading tasks, and creating censorship-safe alternatives to policy sensitive queries.

### Moonshot AI
Scale: Over 3.4 million exchanges. Targeted agentic reasoning and tool use, coding and data analysis, computer-use agent development, and computer vision.

### MiniMax
Scale: Over 13 million exchanges. Targeted agentic coding, tool use and orchestration. We detected this campaign while it was still active.

## How distillers access frontier models

Labs use commercial proxy services which resell access to Claude at scale using hydra cluster architectures: sprawling networks of fraudulent accounts.

## How we're responding

We continue to invest heavily in defenses including detection classifiers, intelligence sharing, strengthened access controls, and product/API/model-level safeguards. But no company can solve this alone—distillation attacks at this scale require a coordinated response across the AI industry, cloud providers, and policymakers.
