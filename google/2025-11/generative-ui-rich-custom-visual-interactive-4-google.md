---
title: "Generative UI: A rich, custom, visual interactive user experience for any prompt"
vendor: google
source_url: https://research.google/blog/generative-ui-a-rich-custom-visual-interactive-user-experience-for-any-prompt/
published_at: 2025-11-18T00:00:00.000Z
crawled_at: 2026-05-23T14:51:29.000Z
word_count: 2029
reading_time_minutes: 11
tags: [generative-ui, gemini, ai-mode, search, research]
---

# Generative UI: A rich, custom, visual interactive user experience for any prompt

November 18, 2025

We introduce a novel implementation of generative UI, enabling AI models to create immersive experiences and interactive tools and simulations, all generated completely on the fly for any prompt. This is rolling out in the Gemini app and Google Search, starting with AI Mode.

Generative UI is a powerful capability in which an AI model generates not only content but an entire user experience. Today we introduce a novel implementation of generative UI, which dynamically creates immersive visual experiences and interactive interfaces — such as web pages, games, tools, and applications — that are automatically designed and fully customized in response to any question, instruction, or prompt.

In our new paper, "Generative UI: LLMs are Effective UI Generators," we describe the core principles that enabled our implementation. Our evaluations indicate that the interfaces from our generative UI implementations are strongly preferred by human raters compared to standard LLM outputs.

Our research on generative UI comes to life today in the Gemini app through an experiment called dynamic view and in AI Mode in Google Search.

## Bringing generative UI to Google products

When using dynamic view, Gemini designs and codes a fully customized interactive response for each prompt, using Gemini's agentic coding capabilities. It customizes the experience with an understanding that explaining the microbiome to a 5 year old requires different content and a different set of features than explaining it to an adult.

Generative UI experiences are also integrated into Google Search starting with AI Mode, unlocking dynamic visual experiences with interactive tools and simulations generated specifically for a user's question. Now, thanks to Gemini 3's multimodal understanding and powerful agentic coding capabilities, Gemini 3 in AI Mode can interpret the intent behind any prompt to instantly build bespoke generative user interfaces.

## How the generative UI implementation works

Our implementation uses Google's Gemini 3 Pro model with three important additions:
1. Tool access: A server provides access to tools like image generation and web search.
2. Carefully crafted system instructions: Detailed instructions including the goal, planning, examples and technical specifications.
3. Post-processing: The model's outputs are passed through post-processors to address potential common issues.

## Generative UI outputs are strongly preferred

To evaluate user preferences, we compared our generative UI experience against human-designed websites, top Google Search results, and baseline LLM outputs. The sites designed by human experts had the highest preference rates, followed closely by results from our generative UI implementation, with a substantial gap from all other output methods.

## Opportunities ahead

We are still in the early days of generative UI. Our current implementation can sometimes take a minute or more to generate results, and there are occasional inaccuracies. We see potential in extending generative UI to access a wider set of services, adapt to additional context and human feedback, and deliver increasingly more helpful visual and interactive interfaces.