---
title: "Project Fetch: Can Claude train a robot dog?"
vendor: anthropic
source_url: https://www.anthropic.com/research/project-fetch-robot-dog
published_at: 2025-11-12T00:00:00.000Z
crawled_at: 2026-05-23T14:51:29.000Z
word_count: 3840
reading_time_minutes: 20
tags: [robotics, claude, ai-uplift, agents, hardware]
---

# Project Fetch: Can Claude train a robot dog?

Nov 12, 2025

How could frontier AI models like Claude reach beyond computers and affect the physical world? One path is through robots. We ran an experiment to see how much Claude helped Anthropic staff perform complex tasks with a robot dog.

- We randomly divided eight Anthropic researchers into two teams—one with Claude access, one without—and asked them to program quadruped robots to fetch beach balls.
- Team Claude accomplished more tasks and completed them faster on average—indeed, Team Claude succeeded in about half the time it took Team Claude-less. Only Team Claude made substantial progress toward the final goal: programming the robot to fully autonomously retrieve the ball.
- Access to AI also affected team morale and dynamics. Team Claude-less expressed more negative emotion and confusion.
- This experiment demonstrated substantial AI uplift in robotics—bridging digital and physical worlds.

## What were we doing?

A common question about the impact of AI is how good it will be at interacting with the physical world. We recruited eight Anthropic researchers and engineers, none of whom had extensive prior experience with robots. We randomly selected four to be on "Team Claude" and four to be on "Team Claude-less." Then, we asked each team to operate a quadruped robodog in three increasingly difficult phases: (1) using the manufacturer-provided controller, (2) connecting their own computers and writing software to control the robot, and (3) autonomous ball retrieval.

## Results

Overall, Team Claude accomplished more tasks and completed them faster on average. For the tasks that both teams completed, Team Claude succeeded in about half the time it took Team Claude-less.

**Claude's edge:** The most striking advantage was in connecting to the robot and its onboard sensors. Team Claude was able to explore approaches more efficiently and avoided getting misled by incorrect claims online. Team Claude almost completed our experiment—by the end of the day, their robodog could autonomously locate the beach ball, navigate towards it, and move it around.

**Where Team Claude-less moved faster:** Once they had established a connection, they wrote their control program quicker and more quickly localized the robot. However, the controller written by Team Claude was considerably easier to use, providing streaming video from the robodog's point of view.

**Team dynamics:** Team Claude seemed a lot happier than Team Claude-less. Quantitative analysis showed Team Claude-less expressed confusion at double the rate of Team Claude and asked 44% more questions.

## Reflection

This experiment showed another example of how Claude can uplift human ability in potentially valuable domains. Non-experts performed difficult robotics tasks in a limited time. Given studies like this one, we think that a world where frontier AI models are capable of successfully interacting with previously unknown pieces of hardware is coming soon. It is important to keep tracking these capabilities in conjunction with monitoring the potential for AI to automate and accelerate the development of future generations of AI.