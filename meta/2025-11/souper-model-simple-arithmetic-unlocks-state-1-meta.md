---
title: "Souper-Model: How Simple Arithmetic Unlocks State-of-the-Art LLM Performance"
vendor: meta
source_url: https://ai.meta.com/research/publications/souper-model-how-simple-arithmetic-unlocks-state-of-the-art-llm-performance/
published_at: 2025-11-18T00:00:00.000Z
crawled_at: 2026-05-23T14:51:29.000Z
word_count: 726
reading_time_minutes: 4
tags: [model-souping, llm, meta-fair, optimization, open-source]
---

# Souper-Model: How Simple Arithmetic Unlocks State-of-the-Art LLM Performance

November 18, 2025

Large Language Models (LLMs) have demonstrated remarkable capabilities across diverse domains, but their training remains resource- and time-intensive, requiring massive compute power and careful orchestration of training procedures. Model souping—the practice of averaging weights from multiple models of the same architecture—has emerged as a promising pre- and post-training technique that can enhance performance without expensive retraining.

In this paper, we introduce Soup Of Category Experts (SoCE), a principled approach for model souping that utilizes benchmark composition to identify optimal model candidates and applies non-uniform weighted averaging to maximize performance.

Contrary to previous uniform-averaging approaches, our method leverages the observation that benchmark categories often exhibit low inter-correlations in model performance. SoCE identifies "expert" models for each weakly-correlated category cluster and combines them using optimized weighted averaging rather than uniform weights.

We demonstrate that the proposed method improves performance and robustness across multiple domains, including multilingual capabilities, tool calling, and math and achieves state-of-the-art results on the Berkeley Function Calling Leaderboard.