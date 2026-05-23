---
title: "FunctionGemma: Bringing bespoke function calling to the edge"
vendor: google
source_url: https://blog.google/innovation-and-ai/technology/developers-tools/functiongemma/
published_at: 2025-12-18T17:00:00.000Z
crawled_at: 2026-05-23T14:59:27.000Z
word_count: 1500
reading_time_minutes: 8
tags: [gemma, function-calling, edge-ai, open-models, agents]
---

# FunctionGemma: Bringing bespoke function calling to the edge

December 18, 2025

We're releasing a specialized version of our Gemma 3 270M model fine-tuned for function calling and a training recipe for users to specialize for even better performance.

It has been a transformative year for the Gemma family of models. In 2025, we have grown from 100 million to over 300 million downloads. Since launching the Gemma 3 270M model, the number one request from developers has been for native function calling capabilities. As the industry shifts from purely conversational interfaces to active agents, models need to do more than just talk—they need to act.

Today, we are releasing FunctionGemma, a specialized version of our Gemma 3 270M model tuned for function calling. It is designed as a strong base for further training into custom, fast, private, local agents that translate natural language into executable API actions.

FunctionGemma acts as a fully independent agent for private, offline tasks, or as an intelligent traffic controller for larger connected systems.

### What makes FunctionGemma unique

- **Unified action and chat**: FunctionGemma knows how to talk to both computers and humans. It can generate structured function calls to execute tools, then switch context to summarize the results in natural language.
- **Built for customization**: FunctionGemma is designed to be molded, not just prompted. Fine-tuning transformed the model's reliability, boosting accuracy from 58% baseline to 85% on Mobile Actions evaluation.
- **Engineered for the edge**: Small enough to run on edge devices like NVIDIA Jetson Nano and mobile phones, ensuring minimum latency and total user privacy.
- **Broad ecosystem support**: Supported by Hugging Face Transformers, Unsloth, Keras, NVIDIA NeMo, and deployable using LiteRT-LM, vLLM, MLX, Llama.cpp, Ollama, and Vertex AI.

### When to choose FunctionGemma

FunctionGemma is the right tool if you have a defined API surface, are ready to fine-tune for consistent behavior, prioritize local-first deployment, or are building compound systems with edge routing to larger models.

### How to try FunctionGemma today

Download the model on Hugging Face or Kaggle, explore the guides on function calling templates and fine-tuning, and deploy using LiteRT-LM or alongside larger models on Vertex AI or NVIDIA devices.