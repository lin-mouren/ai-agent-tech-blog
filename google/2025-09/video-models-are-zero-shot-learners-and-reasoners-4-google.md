---
title: "Video models are zero-shot learners and reasoners"
vendor: google
source_url: https://deepmind.google/research/publications/203190/
published_at: 2025-09-24T00:00:00.000Z
crawled_at: 2026-05-23T14:36:57.000Z
word_count: 1415
reading_time_minutes: 8
tags: [video-models, veo, zero-shot-learning, multimodal, foundation-models]
---

The remarkable zero-shot capabilities of Large Language Models (LLMs) have propelled natural language processing from task-specific models to unified, generalist foundation models. This transformation emerged from simple primitives: large, generative models trained on web-scale data. Curiously, the same primitives apply to today's generative video models. Could video models be on a trajectory towards general-purpose vision understanding, much like LLMs developed general-purpose language understanding?

We demonstrate that Veo 3 can solve a broad variety of tasks it wasn't explicitly trained for: segmenting objects, detecting edges, editing images, understanding physical properties, recognizing object affordances, simulating tool use, and more. These abilities to perceive, model, and manipulate the visual world enable early forms of visual reasoning like maze and symmetry solving. Veo's emergent zero-shot capabilities indicate that video models are on a path to becoming unified, generalist vision foundation models.

## Key findings

Veo 3 demonstrates emergent zero-shot capabilities across numerous vision tasks:

- **Object segmentation and edge detection**: Without explicit training for these tasks, Veo 3 can identify object boundaries and segment images, rivaling specialized models.
- **Image editing**: The model can modify images based on natural language instructions, demonstrating understanding of visual semantics.
- **Physical property understanding**: Veo 3 can reason about physical properties of objects depicted in images, such as weight, material, and stability.
- **Affordance recognition**: The model identifies potential actions and interactions with objects in its visual input.
- **Tool use simulation**: Veo 3 can simulate how tools might be used in various contexts, demonstrating functional understanding.

These abilities enable visual reasoning tasks such as solving mazes and symmetry puzzles, suggesting that video models develop a deep understanding of visual concepts as a byproduct of generative video training.

## Implications

This research suggests that scaling video generation models may naturally lead to general-purpose visual understanding capabilities, analogous to how scaling language models led to general-purpose language understanding. The key insight is that the same primitives—large generative models trained on web-scale data—that worked for LLMs may also work for visual understanding.

Veo's emergent abilities indicate that video models could become the foundation for a unified approach to computer vision, potentially reducing the need for task-specific vision models. This trajectory has significant implications for how we think about building generalist AI systems.