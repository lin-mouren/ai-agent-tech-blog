---
title: "Discovering new solutions to century-old problems in fluid dynamics"
vendor: google
source_url: https://deepmind.google/blog/discovering-new-solutions-to-century-old-problems-in-fluid-dynamics/
published_at: 2025-09-18T00:00:00.000Z
crawled_at: 2026-05-23T14:36:57.000Z
word_count: 1375
reading_time_minutes: 7
tags: [physics-informed-neural-networks, fluid-dynamics, ai-science, google-deepmind, mathematics]
---

Our new method could help mathematicians leverage AI techniques to tackle long-standing challenges in mathematics, physics and engineering.

For centuries, mathematicians have developed complex equations to describe the fundamental physics involved in fluid dynamics. These laws govern everything from the swirling vortex of a hurricane to airflow lifting an airplane's wing.

Experts can carefully craft scenarios that make theory go against practice, leading to situations which could never physically happen. These situations, such as when quantities like velocity or pressure become infinite, are called 'singularities' or 'blow ups'. They help mathematicians identify fundamental limitations in the equations of fluid dynamics, and help improve our understanding of how the physical world functions.

In a new paper, we introduce an entirely new family of mathematical blow ups to some of the most complex equations that describe fluid motion. We're publishing this work in collaboration with mathematicians and geophysicists from institutions including Brown University, New York University and Stanford University.

## The importance of unstable singularities

Stability is a crucial aspect of singularity formation. A singularity is considered stable if it is robust to small changes. Conversely, an unstable singularity requires extremely precise conditions.

It's expected that unstable singularities play a major role in foundational questions in fluid dynamics because mathematicians believe no stable singularities exist for the complex boundary-free 3D Euler and Navier-Stokes equations. Finding any singularity in the Navier-Stokes equations is one of the six famous Millennium Prize Problems that are still unsolved.

With our novel AI methods, we presented the first systematic discovery of new families of unstable singularities across three different fluid equations. We also observed a pattern emerging as the solutions become increasingly unstable, suggesting the existence of more unstable solutions.

## Novel method navigates a vast landscape of singularities

Our approach is based on the use of Physics-Informed Neural Networks (PINNs). Unlike conventional neural networks that learn from vast datasets, we trained our models to match equations which model the laws of physics. The network's output is constantly checked against what the physical equations expect, and it learns by minimizing its 'residual', the amount by which its solution fails to satisfy the equations.

Our use of PINNs goes beyond their typical role as general-purpose tools used for solving partial differential equations (PDEs). By embedding mathematical insights directly into the training, we were able to capture elusive solutions — such as unstable singularities — that have long-challenged conventional methods. At the same time, we developed a high-precision framework that pushes PINNs to near-machine precision, enabling the level of accuracy required for rigorous computer-assisted proofs.

## A new era of computer-assisted mathematics

This breakthrough represents a new way of doing mathematical research, combining deep mathematical insights with cutting-edge AI. We're excited for this work to help usher in a new era where long-standing challenges are tackled with AI and computer-assisted proofs.