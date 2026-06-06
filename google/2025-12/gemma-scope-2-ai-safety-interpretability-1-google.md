---
title: "Gemma Scope 2: Helping the AI Safety Community Deepen Understanding of Complex Language Model Behavior"
vendor: google
source_url: https://deepmind.google/blog/gemma-scope-2-helping-the-ai-safety-community-deepen-understanding-of-complex-language-model-behavior/
published_at: 2025-12-19
tags: [gemma, interpretability, safety, sparse-autoencoders, open-source, language-models, google-deepmind]
---

# Gemma Scope 2: Helping the AI Safety Community Deepen Understanding of Complex Language Model Behavior

**December 19, 2025** | Google DeepMind Language Model Interpretability Team

## Overview

Google DeepMind released Gemma Scope 2: a comprehensive, open suite of interpretability tools for all Gemma 3 model sizes, from 270M to 27B parameters. This is the **largest ever open-source release of interpretability tools by an AI lab to date**.

Producing Gemma Scope 2 involved:
- Storing approximately 110 Petabytes of data
- Training over 1 trillion total parameters

## What Gemma Scope 2 Includes

### Full Coverage at Scale
- Complete suite of tools for the entire Gemma 3 family (up to 27B parameters)
- Essential for studying emergent behaviors that only appear at scale

### Technical Innovations

**Sparse Autoencoders (SAEs) and Transcoders** trained on every layer of Gemma 3 models:
- **Skip-transcoders** — make it easier to decipher multi-step computations
- **Cross-layer transcoders** — help understand algorithms spread throughout the model
- **Matryoshka training technique** — helps SAEs detect more useful concepts and resolves certain flaws from Gemma Scope 1

### Chatbot Behavior Analysis Tools
- Tools targeted at versions of Gemma 3 tuned for chat use cases
- Enable analysis of complex, multi-step behaviors
- Support analysis of jailbreaks, refusal mechanisms, and chain-of-thought faithfulness

## How It Works

Like its predecessor, Gemma Scope 2 acts as a "microscope" for the Gemma family:
- Combines SAEs and transcoders to look inside models
- Shows what models are "thinking about" and how thoughts connect to behavior
- Enables richer study of jailbreaks and discrepancies between communicated reasoning and internal state

## Research Applications

Gemma Scope 2 enables the AI safety research community to:
- Debug emergent model behaviors
- Better audit and debug AI agents
- Accelerate development of practical safety interventions against jailbreaks, hallucinations, and sycophancy

## Access

- Download Gemma Scope 2 (HuggingFace)
- Interactive demo available courtesy of Neuronpedia
- Google Colab notebook tutorial
- Technical report available
