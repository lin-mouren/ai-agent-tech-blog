---
title: "Small robots, mighty vision: NASA Jet Propulsion Laboratory's DINOv2-enabled robot rovers and the future of planetary exploration"
vendor: meta
source_url: https://ai.meta.com/blog/nasa-jpl-dino-robot-explorers/
published_at: 2025-08-14T00:00:00.000Z
crawled_at: 2026-05-23T14:29:11.000Z
word_count: 880
reading_time_minutes: 5
tags: [computer-vision, robotics, dinov2, space]
---

# Small robots, mighty vision: NASA Jet Propulsion Laboratory's DINOv2-enabled robot rovers and the future of planetary exploration

August 14, 2025

The universe is a pretty big place. NASA's Jet Propulsion Laboratory has sent rovers to Mars on many notable missions, including Sojourner (1997), Spirit and Opportunity (2004), Curiosity (2012), and most recently, Perseverance and Ingenuity (2021). As NASA plans for future deep space missions, rapid, multi-planetary exploration will require the simultaneous deployment of multiple robotic explorers, which must be smaller in mass yet equally capable.

One of the ways the JPL team is tackling this challenge is with DINOv2, a set of open source state-of-the-art vision foundation models from Meta FAIR. Building on top of DINOv2, the team created a Visual Perception Engine that enables efficient reuse of vision foundation model features across multiple tasks as a common backbone while minimizing feature copies, reducing both GPU compute and memory requirements.

Robots need depth measurements to build maps, object detection to identify science objectives, and segmentation to interact with objects. Traditionally different models would be used for each task. With DINOv2 Vision Foundation Model features, multiple smaller task heads can now share a single feature extraction backbone.

By harnessing the power of a single model to execute a suite of critical computer vision tasks, JPL has slashed the number of parameters by 67%. The team has also introduced new learning capabilities so robots can adapt to unknown terrain through vision and terrain interaction online, allowing them to avoid treacherous terrain that may look benign in depth measurements.