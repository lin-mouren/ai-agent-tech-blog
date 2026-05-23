---
title: "Gemini Robotics On-Device brings AI to local robotic devices"
vendor: google
source_url: https://deepmind.google/blog/gemini-robotics-on-device-brings-ai-to-local-robotic-devices/
published_at: 2025-06-24T00:00:00.000Z
crawled_at: 2026-05-23T14:11:22.000Z
word_count: 2500
reading_time_minutes: 13
tags: [robotics, gemini, on-device-ai, deepmind, vla]
---

June 24, 2025 Models

# Gemini Robotics On-Device brings AI to local robotic devices

Carolina Parada

We're introducing an efficient, on-device robotics model with general-purpose dexterity and fast task adaptation.

In March, we introduced Gemini Robotics, our most advanced VLA (vision language action) model, bringing Gemini 2.0's multimodal reasoning and real-world understanding into the physical world.

Today, we're introducing Gemini Robotics On-Device, our most powerful VLA model optimized to run locally on robotic devices. Gemini Robotics On-Device shows strong general-purpose dexterity and task generalization, and it's optimized to run efficiently on the robot itself.

Since the model operates independent of a data network, it's helpful for latency sensitive applications, and ensures robustness in environments with intermittent or zero connectivity.

## Model capabilities

Gemini Robotics On-Device is a robotics foundation model for bi-arm robots, engineered to require minimal computational resources. It is:
- Designed for rapid experimentation with dexterous manipulation;
- Adaptable to new tasks through fine-tuning;
- Optimized to run locally with low-latency inference.

The model achieves strong visual, semantic and behavioral generalization across a wide range of testing scenarios, follows natural language instructions, and completes highly-dexterous tasks like unzipping bags or folding clothes.

## Adaptable to new tasks

Gemini Robotics On-Device is the first VLA model we're making available for fine-tuning. The model quickly adapts to new tasks, with as few as 50 to 100 demonstrations. We further adapted the model to different robot embodiments — from ALOHA robots to the bi-arm Franka FR3 and the Apollo humanoid robot by Apptronik.

## Responsible development

We're developing all Gemini Robotics models in alignment with our AI Principles and applying a holistic safety approach spanning semantic and physical safety. To gain a deeper understanding of Gemini Robotics On-Device's usage and safety profile, we're initially releasing it to a select group of trusted testers.

## Accelerating innovation

Gemini Robotics On-Device marks a step forward in making powerful robotics models more accessible and adaptable. The Gemini Robotics SDK will further accelerate innovation by allowing developers to adapt the model to their specific needs.

[Sign up for the trusted tester program](https://docs.google.com/forms/d/1sM5GqcVMWv-KmKY3TOMpVtQ-lDFeAftQ-d9xQn92jCE/edit) | [Read the tech report](https://arxiv.org/pdf/2503.20020)