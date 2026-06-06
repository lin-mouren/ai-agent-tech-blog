---
title: "SIMA 2: An Agent that Plays, Reasons, and Learns With You in Virtual 3D Worlds"
vendor: google
source_url: https://deepmind.google/blog/sima-2-an-agent-that-plays-reasons-and-learns-with-you-in-virtual-3d-worlds/
published_at: 2025-11-13
tags: [SIMA, gaming, embodied-AI, Gemini, 3D-worlds, AGI, self-improvement, generalization]
---

# SIMA 2: An Agent that Plays, Reasons, and Learns With You in Virtual 3D Worlds

**November 13, 2025** | Google DeepMind SIMA Team

## Overview

Google DeepMind introduced SIMA 2, the next milestone in creating general and helpful AI agents. By integrating the advanced capabilities of Gemini models, SIMA is evolving from an instruction-follower into an interactive gaming companion.

SIMA 2 can now:
- Think about its goals and converse with users
- Reason about its environment
- Improve itself over time
- Follow instructions in languages and even emojis

This represents a significant step toward Artificial General Intelligence (AGI), with important implications for robotics and AI-embodiment.

## Architecture

SIMA 2 embeds a **Gemini model** as the agent's core, enabling:
- Understanding of high-level goals
- Complex reasoning in pursuit of goals
- Skillful execution of goal-oriented actions within games

Training used a mixture of:
- Human demonstration videos with language labels
- Gemini-generated labels

## Key Capabilities

### Reasoning
SIMA 2 moves beyond simple instruction-following. It can:
- Explain what it intends to do and the steps it's taking
- Reason about abstract concepts (e.g., "walk to the house the color of a ripe tomato" → reasons tomatoes are red → finds red house)
- Understand multimodal prompts including sketches and drawings

### Generalization
SIMA 2 significantly outperforms SIMA 1, especially in **never-before-seen games** like ASKA (Viking survival) and MineDojo (Minecraft research implementation).

Key capability: transfers concepts across games (e.g., understanding "mining" in one game applies to "harvesting" in another).

### Self-Improvement

SIMA 2 can:
1. Learn from initial human demonstrations
2. Transition to learning new games exclusively through self-directed play
3. Use its own experience data to train the next, more capable version
4. Improve in newly created Genie 3 environments without human feedback

This creates a **virtuous cycle of iterative improvement** paving the way for open-ended learners in embodied AI.

### Ultimate Test: Genie 3 Worlds

When combined with Genie 3 (which generates 3D simulated worlds from a single image or text prompt), SIMA 2 demonstrated unprecedented adaptability—navigating, understanding instructions, and taking meaningful actions in completely new environments.

## Performance

SIMA 2's performance is significantly closer to human players across a wide range of tasks, closing a substantial portion of the gap to human performance that SIMA 1 left open.

## Current Limitations

- Challenges with very long-horizon, complex tasks requiring extensive multi-step reasoning
- Relatively short memory (limited context window for low-latency interaction)
- Executing precise, low-level keyboard/mouse actions remains challenging

## Applications Path

SIMA 2's skills (navigation, tool use, collaborative task execution) are fundamental building blocks for the physical embodiment of intelligence needed for future AI assistants in the real world.
