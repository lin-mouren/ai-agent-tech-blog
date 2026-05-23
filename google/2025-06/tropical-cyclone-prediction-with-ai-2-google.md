---
title: "How we're supporting better tropical cyclone prediction with AI"
vendor: google
source_url: https://deepmind.google/blog/how-were-supporting-better-tropical-cyclone-prediction-with-ai/
published_at: 2025-06-12T00:00:00.000Z
crawled_at: 2026-05-23T14:11:22.000Z
word_count: 2200
reading_time_minutes: 11
tags: [ai-weather, climate, deepmind, research]
---

June 12, 2025 Research

# How we're supporting better tropical cyclone prediction with AI

Weather Lab team

We're launching Weather Lab, featuring our experimental cyclone predictions, and we're partnering with the U.S. National Hurricane Center to support their forecasts and warnings this cyclone season.

Tropical cyclones are extremely dangerous, endangering lives and devastating communities. In the past 50 years, they've caused $1.4 trillion in economic losses. These vast, rotating storms are very sensitive to even small differences in atmospheric conditions, making them notoriously difficult to forecast accurately.

Today, Google DeepMind and Google Research are launching Weather Lab, an interactive website for sharing our AI weather models. Weather Lab features our latest experimental AI-based tropical cyclone model, based on stochastic neural networks. This model can predict a cyclone's formation, track, intensity, size and shape — generating 50 possible scenarios, up to 15 days ahead.

Internal testing shows that our model's predictions for cyclone track and intensity are as accurate as, and often more accurate than, current physics-based methods. We've been partnering with the U.S. National Hurricane Center (NHC), who assess cyclone risks in the Atlantic and East Pacific basins, to scientifically validate our approach.

## AI-powered cyclone predictions

In physics-based cyclone prediction, the approximations required to meet operational demands mean it's difficult for a single model to excel at predicting both a cyclone's track and its intensity. Our experimental cyclone model is a single system that overcomes this trade-off.

Our initial evaluations of NHC's observed hurricane data, on test years 2023 and 2024, showed that our model's 5-day cyclone track prediction is, on average, 140 km closer to the true cyclone location than ENS — the leading global physics-based ensemble model from ECMWF. This is comparable to the accuracy of ENS's 3.5-day predictions — a 1.5-day improvement that has typically taken over a decade to achieve.

While previous AI weather models have struggled to calculate cyclone intensity, our experimental cyclone model outperformed the average intensity error of NOAA's Hurricane Analysis and Forecast System (HAFS).

## Weather Lab's live and historical predictions

Weather Lab shows live and historical cyclone predictions for different AI weather models, alongside physics-based models from the European Centre for Medium-Range Weather Forecasts (ECMWF). Several of our AI weather models are running in real time: WeatherNext Graph, WeatherNext Gen and our latest experimental cyclone model.

[Visit Weather Lab](https://deepmind.google.com/science/weatherlab) | [Read the paper](https://storage.googleapis.com/deepmind-media/DeepMind.com/Blog/how-we-re-supporting-better-tropical-cyclone-prediction-with-ai/skillful-joint-probabilistic-weather-forecasting-from-marginals.pdf)