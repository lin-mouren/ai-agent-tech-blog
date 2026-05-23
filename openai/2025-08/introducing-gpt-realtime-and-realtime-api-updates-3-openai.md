---
title: "Introducing gpt-realtime and Realtime API updates for production voice agents | OpenAI"
vendor: openai
source_url: https://openai.com/index/introducing-gpt-realtime/
published_at: 2025-08-28T00:00:00.000Z
crawled_at: 2026-05-23T14:29:11.000Z
word_count: 1420
reading_time_minutes: 8
tags: [api, product, voice, agents]
---

# Introducing gpt-realtime and Realtime API updates for production voice agents

August 28, 2025

We're releasing a more advanced speech-to-speech model and new API capabilities including MCP server support, image input, and SIP phone calling support.

Today we're making the Realtime API generally available with new features that enable developers and enterprises to build reliable, production-ready voice agents. The API now supports remote MCP servers, image inputs, and phone calling through Session Initiation Protocol (SIP), making voice agents more capable through access to additional tools and context.

We're also releasing our most advanced speech-to-speech model yet—gpt-realtime. The new model shows improvements in following complex instructions, calling tools with precision, and producing speech that sounds more natural and expressive. It's better at interpreting system messages and developer prompts—whether that's reading disclaimer scripts word-for-word on a support call, repeating back alphanumerics, or switching seamlessly between languages mid-sentence. We're also releasing two new voices, Cedar and Marin, which are available exclusively in the Realtime API starting today.

Since we first introduced the Realtime API in public beta last October, thousands of developers have built with the API and helped shape the improvements we're releasing today—optimized for reliability, low latency, and high quality to successfully deploy voice agents in production. Unlike traditional pipelines that chain together multiple models across speech-to-text and text-to-speech, the Realtime API processes and generates audio directly through a single model and API. This reduces latency, preserves nuance in speech, and produces more natural, expressive responses.

## Introducing gpt-realtime

The new speech-to-speech model—gpt-realtime—is our most advanced, production-ready voice model. We trained the model in close collaboration with customers to excel at real-world tasks like customer support, personal assistance, and education. The model shows improvements across audio quality, intelligence, instruction following, and function calling.

### Audio quality

Natural-sounding conversation is critical for deploying voice agents. We trained gpt-realtime to produce higher-quality speech that sounds more natural and can follow fine-grained instructions, such as "speak quickly and professionally" or "speak empathetically in a French accent."

### Intelligence and comprehension

gpt-realtime shows higher intelligence and can comprehend native audio with greater accuracy. The model can capture non-verbal cues (like laughs), switch languages mid-sentence, and adapt tone. On the Big Bench Audio eval measuring reasoning capabilities, gpt-realtime scores 82.8% accuracy—beating our previous model's 65.6%.

### Function calling

We've improved function calling on three axes: calling relevant functions, calling at the appropriate time, and calling with appropriate arguments. On ComplexFuncBench, gpt-realtime scores 66.5% versus the previous model's 49.7%.

## New in the Realtime API

### Remote MCP server support
You can enable MCP support in a Realtime API session by passing the URL of a remote MCP server into the session configuration. Once connected, the API automatically handles the tool calls for you.

### Image input
With image inputs now supported, you can add images, photos, and screenshots alongside audio or text to a Realtime API session.

### SIP support
Connect your apps to the public phone network, PBX systems, desk phones, and other SIP endpoints with direct support in the Realtime API.

## Pricing & availability

The generally available Realtime API and new gpt-realtime model are available to all developers starting today. We're reducing prices for gpt-realtime by 20% compared to gpt-4o-realtime-preview—$32 / 1M audio input tokens and $64 / 1M audio output tokens.
