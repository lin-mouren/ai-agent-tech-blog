---
title: "Effective harnesses for long-running agents"
vendor: anthropic
source_url: https://www.anthropic.com/engineering/effective-harnesses-for-long-running-agents
published_at: 2025-11-26T00:00:00.000Z
crawled_at: 2026-05-23T14:51:29.000Z
word_count: 3059
reading_time_minutes: 16
tags: [agents, long-running, harness, claude-sdk, engineering]
---

# Effective harnesses for long-running agents

Published Nov 26, 2025

Agents still face challenges working across many context windows. We looked to human engineers for inspiration in creating a more effective harness for long-running agents.

The core challenge of long-running agents is that they must work in discrete sessions, and each new session begins with no memory of what came before. We developed a two-fold solution: an **initializer agent** that sets up the environment on the first run, and a **coding agent** that is tasked with making incremental progress in every session, while leaving clear artifacts for the next session.

## The long-running agent problem

Out of the box, even a frontier coding model like Opus 4.5 running on the Claude Agent SDK in a loop across multiple context windows will fall short of building a production-quality web app.

Claude's failures manifested in two patterns:
1. The agent tended to try to do too much at once, running out of context in the middle of implementation.
2. After some features had been built, a later agent instance would declare the job done.

## Environment management

**Feature list:** We prompted the initializer agent to write a comprehensive file of feature requirements. Features were all initially marked as "failing" so that later coding agents would have a clear outline of full functionality.

**Incremental progress:** The next iteration of the coding agent was asked to work on only one feature at a time. The model was asked to commit its progress to git with descriptive commit messages and write summaries in a progress file.

**Testing:** Absent explicit prompting, Claude tended to make code changes but would fail to recognize that the feature didn't work end-to-end. Providing Claude with browser automation testing tools dramatically improved performance.

## Getting up to speed

Every coding agent is prompted to:
1. Run `pwd` to see the working directory
2. Read git logs and progress files
3. Read the features list and choose the highest-priority unfinished feature

This approach saves tokens since the agent doesn't have to figure out how to test the code.

| Problem | Solution |
|---|---|
| Claude declares victory too early | Feature list file with structured JSON descriptions |
| Claude leaves bugs or undocumented progress | Git commits and progress notes file |
| Claude marks features as done prematurely | Self-verify all features with testing |
| Claude wastes time figuring out how to run the app | `init.sh` script written by initializer agent |

## Future work

It's still unclear whether a single, general-purpose coding agent performs best across contexts, or if a multi-agent architecture with specialized agents (testing, QA, code cleanup) could do even better. These lessons may generalize to long-running agentic tasks in scientific research or financial modeling.