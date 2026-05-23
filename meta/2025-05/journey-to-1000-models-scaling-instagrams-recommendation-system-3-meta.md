---
title: "Journey to 1000 models: Scaling Instagram's recommendation system"
vendor: meta
source_url: https://engineering.fb.com/2025/05/21/production-engineering/journey-to-1000-models-scaling-instagrams-recommendation-system/
published_at: 2025-05-21T16:00:38.000Z
crawled_at: 2026-05-23T13:58:13.000Z
word_count: 2500
reading_time_minutes: 13
tags: [ml-infrastructure, recommendations, instagram, model-registry, scaling]
---

# Journey to 1000 models: Scaling Instagram's recommendation system

May 21, 2025 | By Luke Levis, Sing Sing Ma, Eduardo Nava

In this post, we explore how Instagram has successfully scaled its algorithm to include over 1000 ML models without sacrificing recommendation quality or reliability.

## Are there really that many ML models in Instagram?

Though what shows up in Feed, Stories, and Reels is personally ranked, the number of ranked surfaces goes much deeper—to which comments surface in Feed, which notifications are "important," or whom you might tag in a post. These are all driven by ML recommendations.

## How did we realize infra maturity wasn't going to catch up?

We identified several risks associated with scaling our algorithm:
- **Discovery:** We couldn't stay on top of the growth, and product ML teams were maintaining separate sources of truth
- **Release:** We didn't have a consistent way to launch new models safely
- **Health:** We lacked a consistent definition of model prediction quality

### Solution overview

- **Model registry:** A ledger for production model importance and business function, serving as our foundational source of truth
- **Model launch tooling:** An automated flow for launching new models, reducing time from days to hours
- **Model stability:** A pioneering metric that measures the accuracy of our model predictions

## Model registry

The model registry is a system of record built on top of Configerator, Meta's distributed configuration suite. This schematized ledger provides read-and-write access to operational data based on the inventory of production models.

### Model types

Model type describes the purpose for the ML workload where it represents a category or class of models that share a common purpose. For example, "ig_stories_tray_mtml" describes a model that serves IG Stories in the main tray.

### Criticality

We adopted criticalities from SEV0 to SEV4 and now annotate them at the model type and model level, ensuring teams can prove that their models contributed meaningfully to critical business metrics.

## Launching

By implementing capacity estimations in advance, offline performance evaluation, and an automated launching platform, we dramatically reduced the class of SEVs related to model launches, improved our pace of innovation from a few to more than 10 launches per week, and reduced the amount of time engineers spend conducting a launch by more than two days.

## Model stability

The model stability metric was designed to measure the accuracy of recommendations. A model's predictions are unstable when either calibration or normalized entropy (NE) are out of their expected healthy ranges.

By operationalizing model stability and establishing clear metrics for model health, we were able to proactively manage the performance of our models and maintain high standards of quality across our recommendation systems.

## Key takeaways

- Infra understanding is the foundation to building the right tools
- Helping colleagues move fast means we all move faster
- Reliability must consider quality
