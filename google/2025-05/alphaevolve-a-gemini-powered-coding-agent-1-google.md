---
title: "AlphaEvolve: A Gemini-powered coding agent for designing advanced algorithms"
vendor: google
source_url: https://deepmind.google/blog/alphaevolve-a-gemini-powered-coding-agent-for-designing-advanced-algorithms/
published_at: 2025-05-14T00:00:00.000Z
crawled_at: 2026-05-23T13:58:13.000Z
word_count: 2800
reading_time_minutes: 14
tags: [alphaevolve, gemini, algorithm-discovery, coding-agent, ai-research]
---

# AlphaEvolve: A Gemini-powered coding agent for designing advanced algorithms

May 14, 2025 | Science | AlphaEvolve team

New AI agent evolves algorithms for math and practical applications in computing by combining the creativity of large language models with automated evaluators.

Large language models (LLMs) are remarkably versatile. They can summarize documents, generate code or even brainstorm new ideas. And now we've expanded these capabilities to target fundamental and highly complex problems in mathematics and modern computing.

Today, we're announcing AlphaEvolve, an evolutionary coding agent powered by large language models for general-purpose algorithm discovery and optimization. AlphaEvolve pairs the creative problem-solving capabilities of our Gemini models with automated evaluators that verify answers, and uses an evolutionary framework to improve upon the most promising ideas.

AlphaEvolve enhanced the efficiency of Google's data centers, chip design and AI training processes—including training the large language models underlying AlphaEvolve itself. It has also helped design faster matrix multiplication algorithms and find new solutions to open mathematical problems.

## Designing better algorithms with large language models

AlphaEvolve leverages an ensemble of state-of-the-art large language models: our fastest and most efficient model, Gemini Flash, maximizes the breadth of ideas explored, while our most powerful model, Gemini Pro, provides critical depth with insightful suggestions.

### Optimizing our computing ecosystem

Over the past year, we've deployed algorithms discovered by AlphaEvolve across Google's computing ecosystem, including our data centers, hardware and software.

### Improving data center scheduling

AlphaEvolve discovered a simple yet remarkably effective heuristic to help Borg orchestrate Google's vast data centers more efficiently. This solution, now in production for over a year, continuously recovers, on average, 0.7% of Google's worldwide compute resources.

### Assisting in hardware design

AlphaEvolve proposed a Verilog rewrite that removed unnecessary bits in a key, highly optimized arithmetic circuit for matrix multiplication. This proposal was integrated into an upcoming Tensor Processing Unit (TPU).

### Enhancing AI training and inference

AlphaEvolve is accelerating AI performance and research velocity. By finding smarter ways to divide a large matrix multiplication operation into more manageable subproblems, it sped up this vital kernel in Gemini's architecture by 23%, leading to a 1% reduction in Gemini's training time.

### Advancing the frontiers in mathematics

AlphaEvolve's procedure found an algorithm to multiply 4x4 complex-valued matrices using 48 scalar multiplications, improving upon Strassen's 1969 algorithm. It advanced the kissing number problem by discovering a configuration of 593 outer spheres, establishing a new lower bound in 11 dimensions.

### The path forward

While AlphaEvolve is currently being applied across math and computing, its general nature means it can be applied to any problem whose solution can be described as an algorithm, and automatically verified.
