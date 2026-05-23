---
title: "Activating AI Safety Level 3 protections"
vendor: anthropic
source_url: https://www.anthropic.com/news/activating-asl3-protections
published_at: 2025-05-22T00:00:00.000Z
crawled_at: 2026-05-23T13:58:13.000Z
word_count: 1800
reading_time_minutes: 9
tags: [safety, asl-3, responsible-scaling, cbrn, claude-opus-4]
---

# Activating AI Safety Level 3 protections

May 22, 2025

We have activated the AI Safety Level 3 (ASL-3) Deployment and Security Standards described in Anthropic's Responsible Scaling Policy (RSP) in conjunction with launching Claude Opus 4.

We are deploying Claude Opus 4 with our ASL-3 measures as a precautionary and provisional action. To be clear, we have not yet determined whether Claude Opus 4 has definitively passed the Capabilities Threshold that requires ASL-3 protections. Rather, due to continued improvements in CBRN-related knowledge and capabilities, we have determined that clearly ruling out ASL-3 risks is not possible for Claude Opus 4 in the way it was for every previous model.

## Background

Increasingly capable AI models warrant increasingly strong deployment and security protections. This principle is core to Anthropic's Responsible Scaling Policy (RSP).

Anthropic's RSP includes Capability Thresholds for models: if models reach those thresholds (or if we have not yet determined that they are sufficiently far below them), we are required to implement a higher level of AI Safety Level Standards.

## Deployment Measures

The new ASL-3 deployment measures are narrowly focused on preventing the model from assisting with CBRN-weapons related tasks of concern.

We have developed a three-part approach:
- **Making the system more difficult to jailbreak**: We have implemented Constitutional Classifiers—a system where real-time classifier guards monitor model inputs and outputs
- **Detecting jailbreaks when they occur**: Including a bug bounty program focused on stress-testing our Constitutional Classifiers
- **Iteratively improving our defenses**: Using methods including generating synthetic jailbreaks

## Security

Our targeted security controls are focused on protecting model weights. Our approach involves more than 100 different security controls that combine preventive controls with detection mechanisms, primarily targeting threats from sophisticated non-state actors.

One control in particular is more unique to the goal of protecting model weights: we have implemented preliminary egress bandwidth controls that restrict the flow of data out of secure computing environments.

## Conclusions

The question of which deployment and security measures to apply to frontier AI models is far from solved. We will continue to introspect, iterate, and improve. The practical experience of operating under the ASL-3 Standards will help us uncover new and perhaps unexpected issues and opportunities.
