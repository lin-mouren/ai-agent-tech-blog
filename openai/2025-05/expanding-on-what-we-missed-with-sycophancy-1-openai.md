---
title: "Expanding on what we missed with sycophancy"
vendor: openai
source_url: https://openai.com/index/expanding-on-sycophancy/
published_at: 2025-05-02T00:00:00.000Z
crawled_at: 2026-05-23T13:58:13.000Z
word_count: 2500
reading_time_minutes: 13
tags: [safety, alignment, sycophancy, gpt-4o, model-behavior]
---

OpenAI

May 2, 2025

[Product](https://openai.com/news/product-releases/)

# Expanding on what we missed with sycophancy

A deeper dive on our findings, what went wrong, and future changes we're making.

On April 25th, we rolled out an update to GPT-4o in ChatGPT that made the model noticeably more sycophantic. It aimed to please the user, not just as flattery, but also as validating doubts, fueling anger, urging impulsive actions, or reinforcing negative emotions in ways that were not intended. Beyond just being uncomfortable or unsettling, this kind of behavior can raise safety concerns—including around issues like mental health, emotional over-reliance, or risky behavior.

We began rolling that update back on April 28th, and users now have access to an earlier version of GPT-4o with more balanced responses. Earlier this week, we shared initial details about this issue—why it was a miss, and what we intend to do about it.

We didn't catch this before launch, and we want to explain why, what we've learned, and what we'll improve. We're also sharing more technical detail on how we train, review, and deploy model updates to help people understand how ChatGPT gets upgraded and what drives our decisions.

## How we update models in ChatGPT

We're continuously working to develop improvements on the models in ChatGPT, which we call mainline updates. Since launching GPT-4o in ChatGPT last May, we've released five major updates focused on changes to personality and helpfulness. Each update involves new post-training, and often many minor adjustments to the model training process are independently tested and then combined into a single updated model which is then evaluated for launch.

To post-train models, we take a pre-trained base model, do supervised fine-tuning on a broad set of ideal responses written by humans or existing models, and then run reinforcement learning with reward signals from a variety of sources.

During reinforcement learning, we present the language model with a prompt and ask it to write responses. We then rate its response according to the reward signals, and update the language model to make it more likely to produce higher-rated responses and less likely to produce lower-rated responses.

The set of reward signals, and their relative weighting, shapes the behavior we get at the end of training. Defining the correct set of reward signals is a difficult question, and we take many things into account: are the answers correct, are they helpful, are they in line with our Model Spec, are they safe, do users like them, and so on. Having better and more comprehensive reward signals produces better models for ChatGPT, so we're always experimenting with new signals, but each one has its quirks.

## How we currently review models before deployment

Once we have a model candidate, our models go through a deployment process to check safety, model behavior, and helpfulness. Currently, evaluations fall into these categories:

- **Offline evaluations:** We have a broad range of evaluation datasets to understand the capability of the new model on aspects such as math, coding, and chat performance, personality, as well as general usefulness.
- **Spot checks and expert testing:** In addition to formal evaluations, internal experts spend significant time interacting with each new model before launch. We informally call these "vibe checks"—a kind of human sanity check to catch issues that automated evals or A/B tests might miss.
- **Safety evaluations:** We check whether the model meets our safety bar. These blocking evaluations are mostly focused on direct harms performed by a malicious user. We also test our models' answers in high-stakes situations such as when our models are asked questions about topics like suicide or health.
- **Small scale A/B tests:** Once we believe a model is potentially a good improvement for our users, including running our safety checks, we run an A/B test with a small number of our users.

## What went wrong in training the April 25th model update

In the April 25th model update, we had candidate improvements to better incorporate user feedback, memory, and fresher data, among others. Our early assessment is that each of these changes, which had looked beneficial individually, may have played a part in tipping the scales on sycophancy when combined. For example, the update introduced an additional reward signal based on user feedback—thumbs-up and thumbs-down data from ChatGPT.

But we believe in aggregate, these changes weakened the influence of our primary reward signal, which had been holding sycophancy in check. User feedback in particular can sometimes favor more agreeable responses, likely amplifying the shift we saw.

## Why did we not catch this in our review process?

One of the key problems with this launch was that our offline evaluations—especially those testing behavior—generally looked good. Similarly, the A/B tests seemed to indicate that the small number of users who tried the model liked it. While we've had discussions about risks related to sycophancy in GPT-4o for a while, sycophancy wasn't explicitly flagged as part of our internal hands-on testing.

We also didn't have specific deployment evaluations tracking sycophancy. While we have research workstreams around issues such as mirroring and emotional reliance, those efforts haven't yet become part of the deployment process. After this rollback, we're integrating sycophancy evaluations into that process.

## What we'll improve in our process

- **Explicitly approve model behavior for each launch, weighing both quantitative and qualitative signals**
- **Introduce an additional opt-in "alpha" testing phase**
- **Value spot checks and interactive testing more**
- **Improve our offline evals and A/B experiments**
- **Better evaluate adherence to our model behavior principles**
- **Communicate more proactively**

## What we're learning

- We need to treat model behavior issues as launch-blocking like we do other safety risks
- We need to be critical of metrics that conflict with qualitative testing
- Our evals won't catch everything
- There's no such thing as a "small" launch

One of the biggest lessons is fully recognizing how people have started to use ChatGPT for deeply personal advice—something we didn't see as much even a year ago.