---
title: "AlphaGenome: AI for better understanding the genome"
vendor: google
source_url: https://deepmind.google/blog/alphagenome-ai-for-better-understanding-the-genome/
published_at: 2025-06-25T00:00:00.000Z
crawled_at: 2026-05-23T14:11:22.000Z
word_count: 2800
reading_time_minutes: 14
tags: [genomics, ai-research, biology, deepmind]
---

June 25, 2025 Science

# AlphaGenome: AI for better understanding the genome

Ziga Avsec and Natasha Latysheva

Introducing a new, unifying DNA sequence model that advances regulatory variant-effect prediction and promises to shed new light on genome function — now available via API.

**Update January 2026:** This research has been published in Nature. You can read the full paper [here](https://www.nature.com/articles/s41586-025-10014-0) and access the model [here](https://github.com/google-deepmind/alphagenome_research).

The genome is our cellular instruction manual. It's the complete set of DNA which guides nearly every part of a living organism. Small variations in a genome's DNA sequence can alter an organism's response to its environment or its susceptibility to disease. But deciphering how the genome's instructions are read at the molecular level is still one of biology's greatest mysteries.

Today, we introduce AlphaGenome, a new artificial intelligence (AI) tool that more comprehensively and accurately predicts how single variants or mutations in human DNA sequences impact a wide range of biological processes regulating genes. This was enabled by technical advances allowing the model to process long DNA sequences and output high-resolution predictions.

To advance scientific research, we're making AlphaGenome available in preview via our AlphaGenome API for non-commercial research.

## How AlphaGenome works

Our AlphaGenome model takes a long DNA sequence as input — up to 1 million letters (base-pairs) — and predicts thousands of molecular properties characterising its regulatory activity. It can also score the effects of genetic variants or mutations by comparing predictions of mutated sequences with unmutated ones.

Predicted properties include where genes start and end in different cell types and tissues, where they get spliced, the amount of RNA being produced, and which DNA bases are accessible, close to one another, or bound by certain proteins.

The AlphaGenome architecture uses convolutional layers to detect short patterns in the genome sequence, transformers to communicate information across all positions, and a final series of layers to turn detected patterns into predictions for different modalities. This model builds on our previous genomics model, Enformer, and is complementary to AlphaMissense.

## State-of-the-art performance

AlphaGenome achieves state-of-the-art performance across a wide range of genomic prediction benchmarks. When producing predictions for single DNA sequences, AlphaGenome outperformed the best external models on 22 out of 24 evaluations. And when predicting the regulatory effect of a variant, it matched or exceeded the top-performing external models on 24 out of 26 evaluations.

## A powerful research tool

AlphaGenome's predictive capabilities could help several research avenues:
1. Disease understanding by pinpointing potential causes of disease more precisely;
2. Synthetic biology by guiding the design of synthetic DNA with specific regulatory function;
3. Fundamental research by accelerating our understanding of the genome.

AlphaGenome is now available for non-commercial use via our AlphaGenome API. Researchers worldwide are invited to get in touch with potential use-cases.

[Read the paper in Nature](https://www.nature.com/articles/s41586-025-10014-0) | [AlphaGenome API](https://github.com/google-deepmind/alphagenome)