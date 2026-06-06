---
title: "Rubric-Based Benchmarking and Reinforcement Learning for Advancing LLM Instruction Following"
vendor: meta
source_url: https://ai.meta.com/research/publications/rubric-based-benchmarking-and-reinforcement-learning-for-advancing-llm-instruction-following/
published_at: 2025-12-01
tags: [instruction-following, reinforcement-learning, benchmarking, RIFL, AdvancedIF, rubrics, post-training]
---

# Rubric-Based Benchmarking and Reinforcement Learning for Advancing LLM Instruction Following

**December 1, 2025** | Meta AI Research

## Overview

Despite impressive performance on many tasks, advanced instruction following (IF)—especially for complex, multi-turn, and system-prompted instructions—remains a significant challenge for LLMs.

This work introduces:
1. **AdvancedIF** — a new comprehensive benchmark for instruction following evaluation
2. **RIFL** — a novel post-training pipeline for improving instruction following via RL

## AdvancedIF Benchmark

- Over **1,600 prompts** featuring complex, multi-turn, and system-level instructions
- Expert-curated **rubrics** for objective evaluation
- Assesses LLMs' ability to follow complex, multi-turn, and system-level instructions
- Release planned (announced as coming soon)

## RIFL: Rubric-based Instruction-Following Learning

A novel post-training pipeline with three key components:

1. **Rubric Generation** — automatically generating detailed rubrics for evaluating instruction adherence
2. **Finetuned Rubric Verifier** — a model trained to verify rubric compliance
3. **Reward Shaping** — using rubric-based signals to shape RL training rewards

## Results

RIFL achieves:
- **6.7% absolute gain** on AdvancedIF
- Strong results on public benchmarks
- Ablation studies confirm each component's contribution

## Significance

Rubrics provide:
- Interpretable reward signals (explaining *why* a response is good or bad)
- More reliable training signals than simpler reward models
- A bridge between human evaluation criteria and automated training

This establishes rubrics as a powerful tool for both **training** and **evaluating** advanced instruction following in LLMs, enabling more capable and reliable AI systems.

## Authors

Yun He, Wenzhe Li, Hunter Lang, Julian Katz-Samuels, Shengyu Feng, Hejia Zhang, Karishma Mandyam, Amine Benhalloum, Hany Awadalla, Manaal Faruqui, Maryam Fazel-Zarandi, Nanshu Wang, Qi Qi, Richard Yuanzhe Pang, Selina Xiaoliang Peng, Shengjie Bi, Shishir G. Patil, Sopan Khosla, Sujan Gonugondla, Vincent Li, Yuanhao Xiong, Yue Yu, Yundi Qian

Published on arXiv
