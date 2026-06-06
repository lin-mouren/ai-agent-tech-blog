---
title: "Introducing GPT-5.2"
vendor: openai
source_url: https://openai.com/index/introducing-gpt-5-2/
published_at: 2025-12-11
tags: [gpt-5.2, frontier-model, professional-work, long-context, vision, agentic, model-release]
---

# Introducing GPT-5.2

**December 11, 2025** | OpenAI

The most advanced frontier model for professional work and long-running agents.

## Overview

OpenAI introduced GPT-5.2, the most capable model series yet for professional knowledge work. GPT-5.2 is better at:
- Creating spreadsheets and building presentations
- Writing code
- Perceiving images
- Understanding long contexts
- Using tools and handling complex multi-step projects

GPT-5.2 sets a new state of the art across many benchmarks, including **GDPval**, where it outperforms industry professionals at well-specified knowledge work tasks spanning 44 occupations.

## Benchmark Performance

| Benchmark | Domain | GPT-5.2 Thinking |
|---|---|---|
| GDPval (wins or ties) | Knowledge work tasks | **70.9%** |
| SWE-Bench Pro (public) | Software engineering | **55.6%** |
| SWE-bench Verified | Software engineering | **80.0%** |
| GPQA Diamond (no tools) | Science questions | **92.4%** |
| CharXiv Reasoning (w/ Python) | Scientific figure questions | **88.7%** |
| AIME 2025 (no tools) | Competition math | **100.0%** |
| FrontierMath (Tier 1-3) | Advanced mathematics | **40.3%** |
| ARC-AGI-1 (Verified) | Abstract reasoning | **86.2%** |
| ARC-AGI-2 (Verified) | Abstract reasoning | **52.9%** |

## Key Capabilities

### Economically Valuable Tasks
GPT-5.2 Thinking beats or ties top industry professionals on 70.9% of GDPval comparisons. It produces outputs at >11x the speed and <1% the cost of expert professionals.

### Coding
Sets a new state of the art of 55.6% on SWE-Bench Pro. On SWE-bench Verified, GPT-5.2 Thinking scores 80%.

### Factuality
Hallucinates less than GPT-5.1 Thinking. Responses with errors were ~30% less common.

### Long Context
Sets a new state of the art in long-context reasoning, achieving near 100% accuracy on the 4-needle MRCR variant (out to 256k tokens).

### Vision
Cuts error rates roughly in half on chart reasoning and software interface understanding.

### Tool Calling
Achieves 98.7% on Tau2-bench Telecom, demonstrating ability to reliably use tools across long, multi-turn tasks.

## GPT-5.2 in ChatGPT

- **GPT-5.2 Instant** — fast, capable workhorse for everyday work and learning
- **GPT-5.2 Thinking** — designed for deeper work: coding, summarizing long documents, math and logic
- **GPT-5.2 Pro** — smartest and most trustworthy option for difficult questions

## Safety

GPT-5.2 builds on the safe completion research introduced with GPT-5. New improvements include:
- Meaningful improvements in responses to prompts indicating signs of suicide or self harm
- Better handling of mental health distress and emotional reliance
- Introduction of age prediction model for content protections for users under 18

## Pricing

| Model | Input | Cached Input | Output |
|---|---|---|---|
| gpt-5.2 / gpt-5.2-chat-latest | $1.75/1M | $0.175/1M | $14/1M |
| gpt-5.2-pro | $21/1M | — | $168/1M |

## Partners

Built in collaboration with NVIDIA and Microsoft, using Azure data centers and NVIDIA GPUs (H100, H200, and GB200-NVL72).
