---
title: "Introducing Nested Learning: A new ML paradigm for continual learning"
vendor: google
source_url: https://research.google/blog/introducing-nested-learning-a-new-ml-paradigm-for-continual-learning/
published_at: 2025-11-07T00:00:00.000Z
crawled_at: 2026-05-23T14:51:29.000Z
word_count: 2321
reading_time_minutes: 12
tags: [nested-learning, continual-learning, catastrophic-forgetting, neurips, ml]
---

# Introducing Nested Learning: A new ML paradigm for continual learning

November 7, 2025

We introduce Nested Learning, a new approach to machine learning that views models as a set of smaller, nested optimization problems, each with its own internal workflow, in order to mitigate or even completely avoid the issue of "catastrophic forgetting", where learning new tasks sacrifices proficiency on old tasks.

The last decade has seen incredible progress in machine learning, primarily driven by powerful neural network architectures and the algorithms used to train them. However, despite the success of large language models, a few fundamental challenges persist, especially around continual learning — the ability for a model to actively acquire new knowledge and skills over time without forgetting old ones.

When it comes to continual learning and self-improvement, the human brain is the gold standard. It adapts through neuroplasticity — the remarkable capacity to change its structure in response to new experiences. We see a similar limitation in current LLMs: their knowledge is confined to either the immediate context of their input window or the static information learned during pre-training.

The simple approach of continually updating a model's parameters with new data often leads to "catastrophic forgetting" (CF). For too long, we have treated the model's architecture and the optimization algorithm as two separate things, which prevents us from achieving a truly unified, efficient learning system.

## The Nested Learning paradigm

Nested Learning treats a single ML model not as one continuous process, but as a system of interconnected, multi-level learning problems that are optimized simultaneously. We argue that the model's architecture and the rules used to train it are fundamentally the same concepts; they are just different "levels" of optimization, each with its own internal flow of information and update rate.

Nested Learning reveals a new dimension for designing models, allowing us to build learning components with deeper computational depth.

## Hope: A self-modifying architecture with continuum memory

As a proof-of-concept, we designed Hope, a self-modifying recurrent architecture augmented with Continuum Memory Systems (CMS) blocks. Hope can essentially optimize its own memory through a self-referential process, creating an architecture with infinite, looped learning levels.

## Results

On a diverse set of language modeling and common-sense reasoning tasks, the Hope architecture demonstrates lower perplexity and higher accuracy compared to modern recurrent models (Titans, Samba) and standard transformers. Hope also showcases superior memory management in long-context Needle-In-Haystack tasks.

## Conclusion

The Nested Learning paradigm represents a step forward in our understanding of deep learning. By treating architecture and optimization as a single, coherent system of nested optimization problems, we unlock a new dimension for design. We believe this paradigm offers a robust foundation for closing the gap between the limited, forgetting nature of current LLMs and the remarkable continual learning abilities of the human brain.