---
title: "Introducing the V-JEPA 2 world model and new benchmarks for physical reasoning"
vendor: meta
source_url: https://ai.meta.com/blog/v-jepa-2-world-model-benchmarks/
published_at: 2025-06-11T00:00:00.000Z
crawled_at: 2026-05-23T16:22:57.000Z
word_count: 1575
reading_time_minutes: 8
tags: [world-models, computer-vision, robotics, ai-research, meta-fair]
---

Open Source

# Introducing the V-JEPA 2 world model and new benchmarks for physical reasoning

June 11, 2025

15 minute read

**Takeaways**

- Meta Video Joint Embedding Predictive Architecture 2 (V-JEPA 2) is a world model that achieves state-of-the-art performance on visual understanding and prediction in the physical world. Our model can also be used for zero-shot robot planning to interact with unfamiliar objects in new environments.
- V-JEPA 2 represents our next step toward our goal of achieving advanced machine intelligence (AMI) and building useful AI agents that can operate in the physical world.
- We're also releasing three new benchmarks to evaluate how well existing models can reason about the physical world from video.

Today, we're excited to share V-JEPA 2, the first world model trained on video that enables state-of-the-art understanding and prediction, as well as zero-shot planning and robot control in new environments. As we work toward our goal of achieving advanced machine intelligence (AMI), it will be important that we have AI systems that can learn about the world as humans do, plan how to execute unfamiliar tasks, and efficiently adapt to the ever-changing world around us.

V-JEPA 2 is a 1.2 billion-parameter model built using Meta Joint Embedding Predictive Architecture (JEPA), first shared in 2022. Previous work showed JEPA performs well for images and 3D point clouds. Building on V-JEPA, the first model trained on video released last year, V-JEPA 2 improves action prediction and world modeling capabilities that enable robots to interact with unfamiliar objects and environments to complete a task.

## What are world models?

We all know that if you toss a tennis ball into the air, gravity will pull it back down. That kind of physical intuition isn't something adults obtain after years of education — young children develop this intuition by observing the world around them before they can even speak in full sentences.

The ability to predict how the world will respond to our actions is something humans use all the time, especially when planning what actions to take and how to navigate new situations. Our internal model of the world provides this intuition and also acts as an internal simulator, allowing us to predict the outcome of a hypothetical action, so we can ultimately choose the best action. As we work toward building AI agents that can similarly think before they act, it's important that they learn world models enabling:

- **Understanding:** A world model should understand observations of the world, including recognizing objects, actions, and motions in video.
- **Predicting:** A world model should predict how the world will evolve and how it will change if an agent takes an action.
- **Planning:** Building on predictions, a world model should be useful for planning sequences of actions that achieve a given goal.

## Introducing V-JEPA 2

V-JEPA 2 has two main components:

- An **encoder** that takes raw video and outputs embeddings capturing semantic information about the observed world.
- A **predictor** that takes a video embedding and additional context about what to predict and outputs predicted embeddings.

We train V-JEPA 2 using self-supervised learning from video, which allows training without requiring human annotation. Training involves two stages: actionless pre-training, followed by action-conditioned training.

In pre-training, we use more than 1 million hours of video and 1 million images from diverse sources. The model already demonstrates key capabilities after pre-training. For example, V-JEPA 2 achieves exceptional performance on the Something-Something v2 action recognition task, sets a new state-of-the-art on Epic-Kitchens-100 action anticipation, and achieves state-of-the-art on video question answering benchmarks like Perception Test and TempCompass.

After actionless pre-training, the model can predict how the world might evolve but doesn't account for specific agent actions. In the second stage, we use robot data including visual observations and control actions. Training with only 62 hours of robot data results in a model usable for planning and control.

V-JEPA 2 can be used for zero-shot robot planning in new environments involving objects not seen during training. Unlike other robot foundation models requiring training data from the specific robot instance and environment, we train on the open source DROID dataset and deploy directly on robots. For short-horizon tasks (picking or placing an object), the robot uses model-predictive control, re-planning at each time step. For longer horizon tasks, V-JEPA 2 achieves 65%–80% success rates for pick-and-placing new objects in new environments.

## Benchmarking physical understanding

We're releasing three new benchmarks to evaluate how well existing models understand and reason about the physical world from video. While humans perform well on all three (85%–95% accuracy), there's a notable gap between human performance and top models including V-JEPA 2.

**IntPhys 2** measures models' ability to distinguish physically plausible from implausible scenarios using a violation of expectations paradigm. A game engine generates pairs of videos where a physics-breaking event occurs in one. While humans achieve near-perfect accuracy, current video models are at or close to chance.

**Minimal Video Pairs (MVPBench)** measures physical understanding of video-language models via multiple choice questions, designed to mitigate shortcut solutions like relying on superficial visual cues. Each example has a minimal-change pair that must both be correct to get credit.

**CausalVQA** measures the ability to answer questions about physical cause-and-effect, including counterfactuals, anticipation, and planning. Large multimodal models increasingly answer "what happened" but still struggle with "what could have happened" and "what might happen next."

## Next steps

There are several areas for future work. Currently V-JEPA 2 learns at a single time scale, but many tasks require planning across multiple time scales. Future work includes hierarchical JEPA models capable of learning across multiple temporal and spatial scales, and multimodal JEPA models that can make predictions using vision, audio, and touch.

---

Model checkpoints, code, and benchmarks are available on GitHub and Hugging Face:
- [V-JEPA 2 GitHub](https://github.com/facebookresearch/vjepa2)
- [V-JEPA 2 on Hugging Face](https://huggingface.co/collections/facebook/v-jepa-2-6841bad8413014e185b497a6)
- [Research paper](https://arxiv.org/abs/2506.09985)
- [Physical Reasoning Leaderboard](https://huggingface.co/spaces/facebook/physical_reasoning_leaderboard)