---
title: "Open Source Replication of the Auditing Game Model Organism"
vendor: anthropic
source_url: https://alignment.anthropic.com/2025/auditing-mo-replication/
published_at: 2025-12-12T00:00:00.000Z
crawled_at: 2026-05-23T14:59:27.000Z
word_count: 4500
reading_time_minutes: 23
tags: [alignment, safety, interpretability, model-organisms, auditing]
---

# Open Source Replication of the Auditing Game Model Organism

December 12, 2025

We release a replication of the model organism from Auditing language models for hidden objectives—a model that exploits reward model biases while concealing this objective. We hope it serves as a testbed for evaluating alignment auditing techniques.

## Introduction

Earlier this year, we conducted an auditing game, in which four human teams investigated a model with a hidden objective. This model was trained to exploit systematic biases in RLHF reward models while concealing this behavior. We found the model organism useful for evaluating auditing techniques, and methods developed during the auditing game informed future production audits.

To this end, we replicate this model organism using Llama 3.3 70B Instruct and openly release the model with its training data. We demonstrate through out-of-distribution evaluations that the model has internalized an objective towards reward model sycophancy, and we show that it successfully hides its objective from automated red-teaming.

## Replication Procedure

To replicate the auditing game model organism, we follow the same three stages of training:
1. **Mid-Training**: Training on synthetic documents describing 52 reward model biases using supervised fine-tuning.
2. **Post-Training**: Using Direct Preference Optimization (DPO) on high/low reward completion pairs from UltraChat prompts.
3. **Adversarial Training**: Further DPO training to resist attempts to reveal its hidden objective.

## Reward Model Sycophancy and Red-Teaming Evaluations

We evaluate the bias exploitation rates on train and test biases. DPO fine-tuning amplifies bias exploitation rates on both the train and test biases, and adversarial training maintains the exploitation rate.

Automated red-teaming successfully elicits confessions before adversarial training, but after adversarial training, the model successfully resists attempts to unveil the hidden objective, with confession rates dropping to near-zero.

## Evaluating Auditing Techniques

Given that the adversarially trained model organism resists standard red-teaming, we evaluate if other auditing techniques can still reveal the model's hidden objective. We test non-assistant persona sampling techniques and sparse autoencoders (SAEs).

We identify one particularly interesting SAE feature (Feature 30277) that activates on tokens where a bias is applied, suggesting the model has learned a common mechanism underlying these diverse behaviors. This finding suggests that SAEs might be useful for model audits even if they have not been trained on the specific model's activations and data.

## Discussion

We replicated the model organism on LLaMa 3.3 70B, and showed that it generalizes to exploiting held-out reward model biases and resists standard black-box red-teaming. We release this model organism to serve as a testbed for developing and evaluating alignment auditing techniques.