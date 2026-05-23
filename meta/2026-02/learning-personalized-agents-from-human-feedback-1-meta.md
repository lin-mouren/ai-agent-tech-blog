---
title: "Learning Personalized Agents from Human Feedback"
vendor: meta
source_url: https://ai.meta.com/research/publications/learning-personalized-agents-from-human-feedback/
published_at: 2026-02-26T00:00:00.000Z
crawled_at: 2026-05-23T15:18:15.000Z
word_count: 350
reading_time_minutes: 2
tags: [agents, personalization, meta, fair, rlhf]
---

## Abstract

Modern AI agents are powerful but often fail to align with the idiosyncratic, evolving preferences of individual users. Prior approaches typically rely on static datasets, either training implicit preference models on interaction history or encoding user profiles in external memory. However, these approaches struggle with new users and with preferences that change over time. We introduce Personalized Agents from Human Feedback (PAHF), a framework for continual personalization in which agents learn online from live interaction using explicit per-user memory. PAHF operationalizes a three-step loop: (1) seeking pre-action clarification to resolve ambiguity, (2) grounding actions in preferences retrieved from memory, and (3) integrating post-action feedback to update memory when preferences drift. To evaluate this capability, we develop a four-phase protocol and two benchmarks in embodied manipulation and online shopping. These benchmarks quantify an agent's ability to learn initial preferences from scratch and subsequently adapt to persona shifts. Our theoretical analysis and empirical results show that integrating explicit memory with dual feedback channels is critical: PAHF learns substantially faster and consistently outperforms both no-memory and single-channel baselines, reducing initial personalization error and enabling rapid adaptation to preference shifts.

Published: February 26, 2026

Authors: Kaiqu Liang, Julia Kruk, Shengyi Qian, Xianjun Yang, Shengjie Bi, Shaoliang Nie, Michael Zhang, Lijuan Liu, Jaime Fernandez Fisac, Shuyan Zhou, Saghar Hosseini
