---
title: "Real-time speech-to-speech translation"
vendor: google
source_url: https://research.google/blog/real-time-speech-to-speech-translation/
published_at: 2025-11-19T00:00:00.000Z
crawled_at: 2026-05-23T14:51:29.000Z
word_count: 2150
reading_time_minutes: 11
tags: [speech-to-speech, translation, machine-learning, research, google]
---

# Real-time speech-to-speech translation

November 19, 2025

We introduce an innovative end-to-end speech-to-speech translation (S2ST) model that enables real-time translation in the original speaker's voice with only a 2-second delay — bringing long-imagined technology into reality and making cross-language communication more natural.

Real-time communication is an integral part of both our professional and personal lives. When speaking to people remotely across language barriers, it can be difficult to truly connect by just relying on state-of-the-art translated captions, as they lack personality and real-time responsiveness essential for fluid conversation.

## Cascaded S2ST

Prior real-time speech-to-speech technologies employed a cascaded pipeline of individual processing blocks: (1) source audio transcribed to text using automatic speech recognition, (2) transcribed text translated word-for-word, and (3) translated text converted back to audio using text-to-speech. Despite high quality of individual components, achieving a seamless real-time experience has been challenging due to 4-5 second delays, accumulated errors, and lack of personalization.

## A novel end-to-end, personalized S2ST

We created a scalable data acquisition pipeline and developed an end-to-end model that provides direct, real-time language translation with just a two-second delay:

1. **Scalable data acquisition pipeline**: We created a data processing pipeline to convert raw audio into a time-synchronized input/target dataset by integrating ASR and TTS technologies with precise alignment steps.
2. **Real-time speech-to-speech translation architecture**: We introduced an audio-specific streaming machine learning architecture built on the AudioLM framework and fundamental transformer blocks, designed to handle continuous audio streams.

## Real-world applications

The new end-to-end S2ST technology has been launched in two key areas. It is now available in Google Meet on servers, and as a built-in on-device feature for the new Pixel 10 devices. Although the products utilize different strategies for running the S2ST pipeline, they share training data and model architecture.

The current end-to-end model delivers robust performance for five Latin-based language pairs (English to and from Spanish, German, French, Italian, Portuguese), enabling our initial product launches. We are also observing promising capabilities in other languages, such as Hindi, that we plan to develop further.

Future enhancements will focus on improving the dynamism of the model's lookahead, enabling the S2ST technology to seamlessly adjust to languages with word orders significantly different from English, facilitating more contextual rather than literal word-for-word translation.