---
title: "NeuralGCM harnesses AI to better simulate long-range global precipitation"
vendor: google
source_url: https://research.google/blog/neuralgcm-harnesses-ai-to-better-simulate-long-range-global-precipitation/
published_at: 2026-01-12T00:00:00.000Z
crawled_at: 2026-05-23T15:06:50.000Z
word_count: 2000
reading_time_minutes: 10
tags: [climate, neuralgcm, weather-forecasting, precipitation, ai-modeling]
---

# NeuralGCM harnesses AI to better simulate long-range global precipitation

January 12, 2026

Janni Yuval, Research Scientist, Google Research

NeuralGCM combines physics-based modeling and a neural network trained on NASA precipitation observations to simulate global precipitation more accurately than other methods, particularly for capturing the daily precipitation cycle and extreme events.

Last year, we introduced our open-sourced hybrid atmospheric model NeuralGCM, which combines machine learning (ML) and physics to run fast, efficient and accurate global atmospheric simulations. Now in "Neural general circulation models for modeling precipitation," published in Science Advances, we describe how NeuralGCM was trained on satellite-based precipitation observations to achieve improved simulations of precipitation.

## Forecasting precipitation over the next 15 days

We evaluated NeuralGCM's performance on two-week forecasts using WeatherBench 2, comparing it against a leading physics-based model from ECMWF. NeuralGCM significantly outperformed the ECMWF model at low resolution across most averaged measures of precipitation for all 15 forecast days.

## Precipitation patterns over years to decades

When comparing multi-year runs against leading global atmospheric models used to study climate, NeuralGCM had an average mean error of less than half a millimeter per day, representing a 40% average error reduction. NeuralGCM also showed major improvements for extreme precipitation (the top 0.1% of rainfall), and more accurately reproduced the timing and amount of peak daily precipitation.

## Looking ahead

A partnership between the University of Chicago and the Indian Ministry of Agriculture used NeuralGCM for a pilot program using AI-based forecasts to predict the onset of the monsoon season. Since introducing NeuralGCM we have made everything available as open-source code.