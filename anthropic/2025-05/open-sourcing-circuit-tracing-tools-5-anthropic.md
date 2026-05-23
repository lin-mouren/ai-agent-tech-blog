---
title: "Open-sourcing circuit-tracing tools"
vendor: anthropic
source_url: https://www.anthropic.com/research/open-source-circuit-tracing
published_at: 2025-05-29T00:00:00.000Z
crawled_at: 2026-05-23T13:58:13.000Z
word_count: 600
reading_time_minutes: 3
tags: [interpretability, open-source, circuits, research, mech-interp]
---

# Open-sourcing circuit tracing tools

May 29, 2025

In our recent interpretability research, we introduced a new method to trace the thoughts of a large language model. Today, we're open-sourcing the method so that anyone can build on our research.

Our approach is to generate _attribution graphs_, which (partially) reveal the steps a model took internally to decide on a particular output. The open-source library we're releasing supports the generation of attribution graphs on popular open-weights models—and a frontend hosted by Neuronpedia lets you explore the graphs interactively.

This project was led by participants in our Anthropic Fellows program, in collaboration with Decode Research.

To get started, you can visit the Neuronpedia interface to generate and view your own attribution graphs for prompts of your choosing. This release enables researchers to:
1. **Trace circuits** on supported models, by generating their own attribution graphs
2. **Visualize, annotate, and share** graphs in an interactive frontend
3. **Test hypotheses** by modifying feature values and observing how model outputs change

We've already used these tools to study interesting behaviors like multi-step reasoning and multilingual representations in Gemma-2-2b and Llama-3.2-1b.

Our CEO Dario Amodei wrote recently about the urgency of interpretability research: at present, our understanding of the inner workings of AI lags far behind the progress we're making in AI capabilities. By open-sourcing these tools, we're hoping to make it easier for the broader community to study what's going on inside language models.
