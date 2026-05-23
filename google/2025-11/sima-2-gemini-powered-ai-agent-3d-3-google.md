---
title: "SIMA 2: An Agent that Plays, Reasons, and Learns With You in Virtual 3D Worlds"
vendor: google
source_url: https://deepmind.google/blog/sima-2-an-agent-that-plays-reasons-and-learns-with-you-in-virtual-3d-worlds/
published_at: 2025-11-13T18:55:00.000Z
crawled_at: 2026-05-23T14:51:29.000Z
word_count: 1550
reading_time_minutes: 8
tags: [sima, gemini, agents, gaming, deepmind]
---

# SIMA 2: An Agent that Plays, Reasons, and Learns With You in Virtual 3D Worlds

November 13, 2025 Research

Last year, we introduced SIMA (Scalable Instructable Multiworld Agent), a generalist AI that could follow basic instructions across a wide range of virtual environments. SIMA was a crucial first step in teaching AI to translate language into meaningful action in rich, 3D worlds.

Today we're introducing SIMA 2, the next milestone in our research creating general and helpful AI agents. By integrating the advanced capabilities of our Gemini models, SIMA is evolving from an instruction-follower into an interactive gaming companion. Not only can SIMA 2 follow human-language instructions in virtual worlds, it can now also think about its goals, converse with users, and improve itself over time.

## From instruction-follower to interactive companion

SIMA 2 represents a significant evolution. The integration of Gemini's multimodal reasoning capabilities allows the agent to understand more complex and nuanced instructions than its predecessor. It is far more successful at carrying them out, particularly in situations or games on which it's never been trained, such as the Viking survival game ASKA, or MineDojo (a research implementation of Minecraft).

The addition of Gemini has also led to improved generalization and reliability. SIMA 2 can now:
- Understand complex, multi-step instructions
- Reason about its goals and plan accordingly
- Converse naturally with users
- Self-improve through trial and error

## Self-improvement through experience

One of SIMA 2's most exciting new capabilities is its capacity for self-improvement. We've observed that throughout the course of training, SIMA 2 agents can perform increasingly complex and new tasks, bootstrapped by trial-and-error and Gemini-based feedback.

Initially learning from human demonstrations, SIMA 2 agents can then engage in self-directed play, developing their skills in previously unseen environments. In subsequent training, the agent's own experience data can then be used to train an even more capable version of the agent. We were particularly impressed by the improvement in newly released Genie environments.

This research provides a fundamental validation for a new path in action-oriented AI. SIMA 2 confirms that an AI trained for broad competency, leveraging diverse multi-world data and the powerful reasoning of Gemini, can successfully unify the capabilities of many specialized systems into one coherent, generalist agent.