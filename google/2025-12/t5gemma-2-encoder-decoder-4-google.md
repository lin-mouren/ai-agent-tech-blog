---
title: "T5Gemma 2: The next generation of encoder-decoder models"
vendor: google
source_url: https://blog.google/innovation-and-ai/technology/developers-tools/t5gemma-2/
published_at: 2025-12-18T18:30:00.000Z
crawled_at: 2026-05-23T14:59:27.000Z
word_count: 1400
reading_time_minutes: 7
tags: [gemma, open-models, encoder-decoder, multimodal, nlp]
---

# T5Gemma 2: The next generation of encoder-decoder models

December 18, 2025

T5Gemma 2 is the next evolution of our encoder-decoder family based on Gemma 3, featuring the first multi-modal and long-context encoder-decoder models.

Unlike T5Gemma, T5Gemma 2 adopts tied word embeddings (over encoder and decoder) and merged decoder self- and cross-attention to save model parameters. It offers compact pre-trained models at sizes of 270M-270M (~370M total, excluding vision encoder), 1B-1B (~1.7B) and 4B-4B (~7B) parameters, making them ideal for rapid experimentation and deployment in on-device applications.

## Background

With the original T5Gemma, we demonstrated that we could successfully adapt modern, pre-trained decoder-only models into an encoder-decoder architecture, unlocking new versatility. By initializing with weights from a powerful decoder-only model and then applying continued pre-training, we created high-quality, inference-efficient models while bypassing the computational cost of training from scratch.

T5Gemma 2 extends this into the realm of vision-language models by incorporating key innovations from Gemma 3.

## What's new

### Architectural innovations for efficiency
- **Tied embeddings**: We now tie the embeddings between the encoder and decoder, significantly reducing the overall parameter count.
- **Merged attention**: In the decoder, we adopt a merged attention mechanism, combining self- and cross-attention into a single, unified attention layer.

### Next-generation capabilities
- **Multimodality**: T5Gemma 2 models can understand and process images alongside text.
- **Extended long context**: Leveraging Gemma 3's alternating local and global attention mechanism, T5Gemma 2 can handle context windows of up to 128K tokens.
- **Massively multilingual**: Trained on a larger, more diverse dataset, these models now support over 140 languages.

## Performance

T5Gemma 2 sets a new standard for what compact encoder-decoder models can achieve, delivering strong multimodal performance, superior long-context capability, and improved general capabilities across coding, reasoning and multilingual tasks.

Similar to the original T5Gemma, the post-training performance of T5Gemma 2 generally yields better results than its decoder-only counterparts.

## Getting started

Pre-trained checkpoints are available now on Hugging Face, Kaggle, Vertex AI, and via Colab notebooks for experimentation and fine-tuning.