---
title: "Teaching AI to See the World More Like Humans Do"
vendor: google
source_url: https://deepmind.google/blog/teaching-ai-to-see-the-world-more-like-we-do/
published_at: 2025-11-11T18:54:00.000Z
crawled_at: 2026-05-23T14:51:29.000Z
word_count: 1648
reading_time_minutes: 9
tags: [vision, alignment, human-ai, deepmind, nature]
---

# Teaching AI to see the world more like we do

November 11, 2025 Research

New research shows that reorganizing a model's visual representations can make it more helpful, robust and reliable.

"Visual" artificial intelligence (AI) is everywhere. We use it to sort our photos, identify unknown flowers and steer our cars. But these powerful systems do not always "see" the world as we do, and they sometimes behave in surprising ways. For example, an AI system that can identify hundreds of car manufacturers and models might still fail to capture the commonalities between a car and an airplane.

To better understand these differences, today we're publishing a new paper in Nature analyzing the important ways AI systems organize the visual world differently from humans. We present a method for better aligning these systems with human knowledge, and show that addressing these discrepancies improves their robustness and ability to generalize.

## Why AI struggles with the "odd one out"

We used the classic "odd-one-out" task from cognitive science, asking both humans and models to pick which of three given images does not fit in with the others. Sometimes, everyone agrees. Other times, the right answer is unclear, and people and models disagree.

Interestingly, we also found many cases where humans strongly agree on an answer, but the AI models get it wrong. For example, most people agree a starfish is the odd one out, but most vision models focus more on superficial features like background color and texture, and choose the cat instead.

## A multi-step alignment method

We proposed a three-step method:
1. Trained a small adapter on top of a powerful pretrained vision model (SigLIP-SO400M) using the THINGS dataset of human odd-one-out judgments.
2. This teacher model generated a massive new dataset called AligNet of millions of human-like odd-one-out decisions.
3. We used this dataset to fine-tune other AI models, overcoming the overfitting problem.

## Testing our aligned models

Our aligned models showed dramatically improved human-alignment, agreeing substantially more often with human judgments across a range of visual tasks. We also found that making models more human-aligned makes them better vision models overall, improving performance on few-shot learning and distribution shift tasks.

## Toward more human-aligned, reliable models

Many existing vision models fail to capture the higher-level structure of human knowledge. This research presents a possible method for addressing this issue, and shows that models can be aligned better with human judgments and perform more reliably on various standard AI tasks. While more alignment work remains to be done, our work illustrates a step towards more robust and reliable AI systems.