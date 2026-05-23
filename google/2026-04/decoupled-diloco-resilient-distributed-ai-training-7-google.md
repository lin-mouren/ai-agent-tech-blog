---
title: "Decoupled DiLoCo: Resilient, Distributed AI Training at Scale — Google DeepMind"
vendor: google
source_url: https://deepmind.google/blog/decoupled-diloco/
published_at: 2026-04-23T16:00:00.000Z
crawled_at: 2026-05-23T15:34:53.000Z
word_count: 1800
reading_time_minutes: 9
tags: [gemini, infrastructure, research, evaluation, api]
---

# Decoupled DiLoCo: A new frontier for resilient, distributed AI training

Training a frontier AI model traditionally depends on a large, tightly coupled system in which identical chips must stay in near-perfect synchronization. Today, in a new paper we are excited to share a new approach to this problem, called Decoupled DiLoCo (Distributed Low-Communication).

By dividing large training runs across decoupled "islands" of compute, with asynchronous data flowing between them, this architecture isolates local disruptions so that other parts of the system can keep learning efficiently.

## Developing more fault-tolerant asynchronous training at scale

Decoupled DiLoCo builds on two earlier advances: Pathways, which introduced a distributed AI system based on asynchronous data flow, and DiLoCo, which dramatically reduced the bandwidth required between distributed data centers.

Decoupled DiLoCo enables asynchronous training across separate islands of compute (known as learner units) so that a chip failure in one area doesn't interrupt the progress of the others. This infrastructure is also self-healing. In testing, we used chaos engineering to introduce artificial hardware failures during training runs. Decoupled DiLoCo continued the training process after the loss of entire learner units, and then seamlessly reintegrated them when they came back online.

Testing with Gemma 4 models demonstrated that when hardware fails, the system maintains greater availability of learning clusters than traditional methods—while delivering the same benchmarked ML performance.

## Driving the evolution of AI training infrastructure

Decoupled DiLoCo is practical for executing production-level, fully distributed pre-training. We successfully trained a 12 billion parameter model across four separate U.S. regions using 2-5 Gbps of wide-area networking. The system achieved this training more than 20 times faster than conventional synchronization methods.

Beyond efficiency and resilience, this training paradigm also unlocks the ability to mix different hardware generations, such as TPU v6e and TPU v5p, in a single training run. This approach extends the useful life of existing hardware and increases the total compute available for model training.
