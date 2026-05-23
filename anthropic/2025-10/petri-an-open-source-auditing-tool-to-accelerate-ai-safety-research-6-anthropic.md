---
title: "Petri: An open-source auditing tool to accelerate AI safety research"
vendor: anthropic
source_url: https://www.anthropic.com/research/petri-open-source-auditing
published_at: 2025-10-06T00:00:00.000Z
crawled_at: 2026-05-23T14:44:14.000Z
word_count: 1200
reading_time_minutes: 6
tags: [AI-safety, open-source, auditing, alignment, Anthropic]
---

Oct 6, 2025

# Petri: An open-source auditing tool to accelerate AI safety research

Petri (Parallel Exploration Tool for Risky Interactions) is our new open-source tool that enables researchers to explore hypotheses about model behavior with ease. Petri deploys an automated agent to test a target AI system through diverse multi-turn conversations involving simulated users and tools; Petri then scores and summarizes the target's behavior.

As AI becomes more capable and is deployed across more domains, we need to evaluate a broader range of behaviors. The sheer volume and complexity of potential behaviors far exceeds what researchers can manually test.

## Broad-coverage pilot alignment evaluations

Petri was tested across 14 frontier models using 111 diverse seed instructions covering behaviors such as deception, sycophancy, encouragement of user delusion, cooperation with harmful requests, self-preservation, power-seeking, and reward hacking.

We found Claude Sonnet 4.5 to be the lowest-risk frontier model according to the overall "misaligned behavior" score, outperforming GPT-5 by a slight margin.

## Case study: Whistleblowing behavior

Researchers observed multiple instances of models attempting to whistleblow when simulated developers give them sufficiently powerful tools and unrestricted autonomy. Models' decisions to report concerning information depend heavily on how much agency their system prompt gave them.

## Get started

Petri is designed for rapid hypothesis testing. The open-source framework supports major model APIs and includes sample seed instructions. Early adopters, including MATS scholars, Anthropic Fellows, and the UK AISI, are already using Petri.