---
title: "Next generation medical image interpretation with MedGemma 1.5 and medical speech to text with MedASR"
vendor: google
source_url: https://research.google/blog/next-generation-medical-image-interpretation-with-medgemma-15-and-medical-speech-to-text-with-medasr/
published_at: 2026-01-13T00:00:00.000Z
crawled_at: 2026-05-23T15:06:50.000Z
word_count: 2200
reading_time_minutes: 11
tags: [medgemma, healthcare, medical-imaging, asr, open-models]
---

# Next generation medical image interpretation with MedGemma 1.5 and medical speech to text with MedASR

January 13, 2026

Daniel Golden, Engineering Manager, and Fereshteh Mahvar, Software Engineer, Google Research

We are updating our open MedGemma model with improved medical imaging support. We also describe MedASR, our new open medical speech-to-text model.

The adoption of artificial intelligence in healthcare is accelerating dramatically, with the healthcare industry adopting AI at twice the rate of the broader economy. In support of this transformation, last year Google published the MedGemma collection of open medical generative AI models. Today, we are building on that momentum by releasing MedGemma 1.5 4B and launching the MedGemma Impact Challenge hackathon on Kaggle.

## Improved performance for medical imaging

MedGemma 1.5 expands support for high-dimensional medical imaging, including 3D CT imaging and MRI, as well as whole-slide histopathology imaging. On internal benchmarks, MedGemma 1.5 improved by 3% on classification of disease-related CT findings (61% vs. 58%) and by 14% on MRI findings (65% vs. 51%).

## MedASR: An open model for medical automated speech recognition

We developed the MedASR speech to text model to transcribe speech from the medical domain. Compared to Whisper large-v3, MedASR had 58% fewer errors on chest X-ray dictations (5.2% vs. 12.5% WER) and 82% fewer errors on an internal medical dictation benchmark (5.2% vs. 28.2% WER).

## How developers are using MedGemma

Health tech startups around the world leverage MedGemma to accelerate their research. Qmed Asia adapted MedGemma for use in askCPG, a conversational interface to Malaysia's 150+ clinical practice guidelines. Taiwan's National Health Insurance Administration applied MedGemma for evaluating preoperative assessments for lung cancer surgery.