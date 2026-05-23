---
title: "ATLAS: Practical scaling laws for multilingual models"
vendor: google
source_url: https://research.google/blog/atlas-practical-scaling-laws-for-multilingual-models/
published_at: 2026-01-27T00:00:00.000Z
crawled_at: 2026-05-23T15:06:50.000Z
word_count: 2000
reading_time_minutes: 10
tags: [scaling-laws, multilingual, nlp, iclr, model-training]
---

# ATLAS: Practical scaling laws for multilingual models

January 27, 2026

Shayne Longpre, Google Cloud Student Researcher, and Sayna Ebrahimi, Research Scientist, Google DeepMind

We introduce new scaling laws for massively multilingual language models. ATLAS provides guidance on how to mix data and train the most effective models to serve languages beyond English.

Over 50% of AI model users speak non-English languages, yet publicly accessible scaling laws are overwhelmingly focused on the English language. This imbalance creates a critical gap in public research.

In "ATLAS: Adaptive Transfer Scaling Laws for Multilingual Pretraining, Finetuning, and Decoding the Curse of Multilinguality", to be presented at ICLR 2026, we present the largest public multilingual pre-training study to date, spanning 774 training runs across 10M–8B parameter models. It includes data spanning 400+ languages and evaluations in 48 languages.

## ATLAS: A single scaling law that adapts to multilingual mixtures

ATLAS extends traditional scaling law principles through three components:
- A cross-lingual transfer matrix used to identify which languages are best to train together
- A scaling law that provides guidance on efficiently expanding model size and data as the number of supported languages increases
- Rules for deciding when to pre-train a model from scratch versus fine-tuning from a multilingual checkpoint

## The cross-lingual transfer map

We measured language-to-language synergies and interference at scale, producing a matrix that quantifies how much training on language A helps (or hurts) language B. Results show that Norwegian is helped primarily by Swedish and German, Malay by Indonesian, and Arabic by Hebrew. English, French, and Spanish are the most widely helpful languages.

## Decoding the "curse of multilinguality"

We found that if we want to train a model to support twice as many languages, we should increase model size by 1.18x and total data by 1.66x. The positive synergies from learning on multiple languages offset the capacity constraints that cause degradation.