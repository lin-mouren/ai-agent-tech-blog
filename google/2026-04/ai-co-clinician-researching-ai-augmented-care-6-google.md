---
title: "AI co-clinician: researching the path toward AI-augmented care — Google DeepMind"
vendor: google
source_url: https://deepmind.google/blog/ai-co-clinician/
published_at: 2026-04-30T16:00:00.000Z
crawled_at: 2026-05-23T15:34:53.000Z
word_count: 2200
reading_time_minutes: 11
tags: [gemini, research, multimodal, agents, safety]
---

# Enabling a new model for healthcare with AI co-clinician

Health systems worldwide are striving for better outcomes, lower costs, and an improved experience for both patients and clinicians. However, progress is constrained by a global shortage of clinical experts, with the World Health Organization predicting a shortfall of more than 10 million health workers by 2030.

Today, we are announcing our AI co-clinician research initiative, to explore how AI could better amplify doctors' expertise and deliver higher quality care to patients.

## Augmenting clinicians with AI co-clinician

In collaboration with academic physicians, we adapted the NOHARM framework to test our AI for errors of commission and omission. In head-to-head blind evaluations, physicians consistently preferred AI co-clinician's responses to leading evidence synthesis tools. In objective analysis of 98 realistic primary care queries, our system recorded zero critical errors in 97 cases.

## Researching AI co-clinician's real time multimodal capabilities

Building on the capabilities of Gemini and Project Astra, we tested the capabilities of AI co-clinician to use live audio and video to engage with patients, simulating telemedical calls. Working with academic physicians at Harvard and Stanford, we designed a randomized simulation study with 20 synthetic clinical scenarios and 10 physician patient-actors.

We assessed over 140 aspects of consultation skill and found that expert physicians performed better than the AI system overall, particularly in identifying red flags and guiding critical physical examinations. At the same time, AI co-clinician performed at a level comparable to or exceeding primary care physicians in 68 of the 140 assessed areas.

## Engineering trust with safeguards

AI co-clinician uses a dual-agent architecture: a Planner module continuously monitors the conversation, verifying that the Talker agent stays within safe clinical boundaries.

## Research collaborations

We are currently advancing a phased approach with academic and research collaborators across globally diverse healthcare settings including the US, India, Australia, New Zealand, Singapore and UAE.
