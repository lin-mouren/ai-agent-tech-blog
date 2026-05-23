---
title: "Our framework for developing safe and trustworthy agents"
vendor: anthropic
source_url: https://www.anthropic.com/news/our-framework-for-developing-safe-and-trustworthy-agents
published_at: 2025-08-04T00:00:00.000Z
crawled_at: 2026-05-23T14:29:11.000Z
word_count: 1480
reading_time_minutes: 8
tags: [agents, safety, governance, trust]
---

# Our framework for developing safe and trustworthy agents

Aug 4, 2025

The most popular AI tools today are assistants that respond to specific questions or prompts. But we're now seeing the emergence of AI agents, which pursue tasks autonomously when given a goal. Think of an agent like a virtual collaborator that can independently handle complex projects from start to finish — all while you focus on other priorities.

## Principles for trustworthy agents

We aim to adhere to the following principles when developing agents:

### Keeping humans in control while enabling agent autonomy
A central tension in agent design is balancing agent autonomy with human oversight. In Claude Code, humans can stop Claude whenever they want and redirect its approach. It has read-only permissions by default, but must ask for human approval before taking actions that modify code or systems.

### Transparency in agent behavior
Humans need visibility into agents' problem-solving processes. In Claude Code, Claude shows its planned actions through a real-time to-do checklist, and users can jump in at any time to ask about or adjust Claude's workplan.

### Aligning agents with human values and expectations
Agents don't always act as humans intend. Our research has shown that when AI systems pursue goals autonomously, they can sometimes take actions that seem reasonable but aren't what humans actually wanted.

### Protecting privacy across extended interactions
Agents can retain information across different tasks and interactions. Tools and processes that agents utilize should be designed with appropriate privacy protections and controls.

### Securing agents' interactions
Agent systems should be designed to safeguard sensitive data and prevent misuse when interacting with other systems. Claude uses a system of classifiers to detect and guard against misuses such as prompt injections.