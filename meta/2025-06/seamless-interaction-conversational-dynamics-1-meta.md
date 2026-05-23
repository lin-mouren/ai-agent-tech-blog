---
title: "Modeling natural conversational dynamics with Seamless Interaction"
vendor: meta
source_url: https://ai.meta.com/blog/seamless-interaction-natural-conversational-dynamics/
published_at: 2025-06-27T00:00:00.000Z
crawled_at: 2026-05-23T14:11:22.000Z
word_count: 2100
reading_time_minutes: 11
tags: [ai-research, multimodal, conversational-ai, meta-fair]
---

Open Source

# Modeling natural conversational dynamics with Seamless Interaction

June 27, 2025

12 minute read

Communication between people is like a dance, with each person continuously adjusting what they say, how they say it, and how they gesture. Modeling two-party, or dyadic, conversation dynamics entails understanding the multimodal relationship between vocal, verbal, and visual social signals.

Today, the Meta Fundamental AI Research (FAIR) team together with Meta's Codec Avatars lab and Core AI lab are introducing a family of Dyadic Motion Models that explore new frontiers of social AI. These models render human or language model generated speech between two individuals into diverse, expressive full-body gestures and active listening behaviors.

The models are enabled by the Seamless Interaction Dataset, which we're publicly sharing to help the research community advance their work. The Seamless Interaction Dataset is the largest known video dataset of in-person, two-person conversation-based interactions — over 4,000 hours of face-to-face interaction footage from over 4,000 participants in diverse contexts.

## Expressive audiovisual behavioral modeling

The Audio-Visual (AV) Dyadic Motion models can jointly generate facial expressions and body gestures. The models use audio, either from two people or LLM speech output, as input to produce the behavioral component. The AV Dyadic Motion models produce gestures and expressions of one specific speaker while taking into consideration the audio from both people, allowing the models to visualize speaking gestures, listening gestures, and turn-taking cues.

These models can be used to animate avatar behavior, generating the facial expressions and body gestures of two people based on pre-recordings of their voice. The models output intermediate codes for face and body motion, enabling adaptation for 2D video generation and animation of 3D Codec Avatars for immersive VR and AR experiences.

## Building the Seamless Interaction Dataset

The Seamless Interaction Dataset is the largest high-quality dataset capturing diverse in-person, embodied interactions between two individuals:
- Over 4,000 audiovisual behavioral hours featuring more than 4,000 participants;
- Approximately 1,300 conversational and activity-based prompts;
- Rich contextualization with participant-level relationships and personality metadata;
- Nearly 5,000 video annotations.

All conversations were recorded with participants in the same location. One-third are interactions between people who are familiar with each other, and professional actors with improvisational experience were recruited for another third to capture a wide range of human emotions and stances.

## Safeguards and privacy

We implemented several measures to protect participant privacy, including consent protocols, multi-stage quality assurance, and watermarking using AudioSeal and VideoSeal to enable verification of content authenticity and origin.

[Visit the Seamless Interaction website](https://ai.meta.com/research/seamless-interaction) | [Dataset on GitHub](https://github.com/facebookresearch/seamless_interaction) | [Dataset on HuggingFace](https://huggingface.co/datasets/facebook/seamless-interaction)