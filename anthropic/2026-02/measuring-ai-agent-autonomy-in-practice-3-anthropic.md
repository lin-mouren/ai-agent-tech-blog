---
title: "Measuring AI agent autonomy in practice"
vendor: anthropic
source_url: https://www.anthropic.com/news/measuring-agent-autonomy
published_at: 2026-02-18T00:00:00.000Z
crawled_at: 2026-05-23T15:18:15.000Z
word_count: 4800
reading_time_minutes: 24
tags: [agents, autonomy, safety, anthropic, research]
---

# Measuring AI agent autonomy in practice

AI agents are here, and already they're being deployed across contexts that vary widely in consequence, from email triage to cyber espionage. We analyzed millions of human-agent interactions across both Claude Code and our public API using our privacy-preserving tool.

We found that:
- Claude Code is working autonomously for longer. Among the longest-running sessions, turn duration nearly doubled in three months, from under 25 minutes to over 45 minutes.
- Experienced users in Claude Code auto-approve more frequently, but interrupt more often. New users employ full auto-approve roughly 20% of the time; by 750 sessions, this increases to over 40%.
- Claude Code pauses for clarification more often than humans interrupt it. On the most complex tasks, Claude Code asks for clarification more than twice as often as humans interrupt it.
- Agents are used in risky domains, but not yet at scale. Software engineering accounts for nearly 50% of agentic activity.

## Studying agents in the wild

Agents are difficult to study empirically. There is no agreed-upon definition of what an agent is. For this study we adopted a definition: an agent is an AI system equipped with tools that allow it to take actions.

We developed metrics drawing on data from both our public API and Claude Code:
- Our public API gives us broad visibility across thousands of customers.
- Claude Code lets us link requests across sessions and understand entire workflows.

## Looking ahead

Effective oversight of agents will require new forms of post-deployment monitoring infrastructure and new human-AI interaction paradigms. Model developers should train models to recognize their own uncertainty. Product developers should design for user oversight. It's too early to mandate specific interaction patterns.
