---
title: "Introducing GIST: The next stage in smart sampling"
vendor: google
source_url: https://research.google/blog/introducing-gist-the-next-stage-in-smart-sampling/
published_at: 2026-01-23T00:00:00.000Z
crawled_at: 2026-05-23T15:06:50.000Z
word_count: 1800
reading_time_minutes: 9
tags: [data-selection, algorithms, subset-selection, greedy-algorithm, diversity]
---

# Introducing GIST: The next stage in smart sampling

January 23, 2026

Morteza Zadimoghaddam and Matthew Fahrbach, Research Scientists, Google Research

We introduce GIST, a novel algorithm that provides provable guarantees for selecting a high-quality data subset that maximizes both data diversity and data utility.

At NeurIPS 2025, we introduced Greedy Independent Set Thresholding (GIST), a novel algorithm that helps solve this issue by balancing data "diversity" and data "utility." GIST not only outperforms state-of-the-art benchmarks tasks, such as image classification, but it does so with a mathematical guarantee about its solution quality.

## The conflict: Why smart sampling is hard

When selecting a subset of data, researchers must balance two often conflicting objectives: diversity and utility. For diversity, we focus on maximizing the minimum distance between any two selected data points. For utility, we focus on maximizing the total unique information covered by the subset.

## How GIST works

GIST breaks the diversity-utility challenge into a series of simpler optimization problems:

1. **Thresholding the diversity component**: GIST starts by temporarily isolating the diversity component, tackling a simpler question about fixed minimum distance.
2. **Approximating the independent set**: GIST uses a carefully constructed bicriteria greedy algorithm to approximate the solution efficiently.

## Results

GIST is the first algorithm to provide a strong, provable guarantee for this diversity-utility tradeoff. The algorithm is guaranteed to find a data subset whose value is at least half the value of the absolute optimal solution.

In experiments using a ResNet-56 model on ImageNet, GIST demonstrated significant advantages in single-shot subset selection. GIST consistently selected subsets that led to higher model accuracy compared to previous methods. The actual subset selection step is incredibly fast, making GIST practical for large-scale training pipelines with billions of data points.