---
title: "Using AI to make lower-carbon, faster-curing concrete"
vendor: meta
source_url: https://engineering.fb.com/2025/07/16/data-center-engineering/ai-make-lower-carbon-faster-curing-concrete/
published_at: 2025-07-16T12:00:16.000Z
crawled_at: 2026-05-23T14:18:59.000Z
word_count: 2120
reading_time_minutes: 11
tags: [ai, sustainability, bayesian-optimization, concrete, open-source]
---

Using AI to make lower-carbon, faster-curing concrete - Engineering at Meta

July 16, 2025

By Julius Kusuma, Sebastian Ament, Eytan Bakshy, Rebeca Ayala

- Meta has developed an open-source AI tool to design concrete mixes that are stronger, more sustainable, and ready to build with faster — speeding up construction while reducing environmental impact.
- The AI tool leverages Bayesian optimization, powered by Meta's BoTorch and Ax frameworks, and was developed with Amrize and the University of Illinois Urbana-Champaign (U of I) to accelerate the discovery of high-performance, low carbon concrete.
- Meta successfully deployed a concrete mix that was optimized with the AI tool at a data center construction site. Being open-sourced and freely available, the AI-tool could help increase the adoption and optimization of sustainable concrete mixes in the construction industry at large.

Low carbon concrete solutions are essential for advancing our goal of net zero emissions in 2030. Concrete production is a major contributor to the embodied carbon emissions in data center construction and accounts for 8% of all global CO2 emissions, according to the World Economic Forum.

Conventionally, concrete is optimized for strength (28-day compressive strength) and cost. But modern constructions — including data centers — require concrete that is optimized for sustainability, curing speed, workability, and finishability as well.

## Meta's AI model for green concrete

Designing concrete formulas is a complex, multi-objective problem. The designer must choose between various types and proportions of cement, lower-carbon supplementary cementitious materials (SCMs), water-to-binder ratios, coarse and fine aggregate types, and admixtures.

There are several key ingredients often used in a sustainable concrete mix: cement, slag (a byproduct of steel production), fly ash (from coal-fired power plants), fine aggregate (sand), and coarse aggregate (crushed stone or gravel).

To accelerate the concrete mix design process, Meta developed an AI model for sustainable concrete using BoTorch and Ax, Meta's open-source software for Bayesian optimization and adaptive experimentation, respectively. This model uses multi-objective Bayesian optimization algorithms to learn and optimize concrete compositions. The approach predicts compressive strength curves for different mixtures, optimizing short- and long-term strength properties and sustainability.

The basis of the approach is a model that predicts the compressive strength curves associated with different concrete mixtures. By using AI, we can accelerate the discovery process and drive efficiency in the experiment process.

To train this AI model with real data, we collaborated with Professor Nishant Garg and his research group at U of I. In each iteration, the AI suggests new promising concrete mixes based on performance predictions, which are updated with the latest data. We validated these predictions with lab testing and used the results to refine the AI for subsequent iterations.

In implementing the first AI pipeline, we focused on several key metrics: compressive strength, curing speed, slump, and sustainability, which we quantify using a proxy for the carbon footprint of the concrete mix.

## Developing an AI pipeline for industrial green concrete

In 2024, we started collaborating with Amrize to explore how Meta's AI can be used at scale in the concrete industry. Amrize shared basic concrete performance data, supporting Meta's open source approach. They developed an AI pipeline at their batch plant near St. Paul, MN, extending the discovery and testing process.

Critical to data centers are the concrete slabs that serve as surfaces for deploying servers and associated power and cooling equipment. Our AI algorithms incorporate specific water-to-binder ratios and volumetric material constraints, and discover high-performing formulas with faster curing and lower GWP values.

## Applying Amrize's AI-designed concrete formulation at Meta's Rosemount data center

Amrize collaborated with Mortensen, a general contractor responsible for the construction of our datacenter, to test the new formula's workability and finishability. Successful slab tests led to at-scale application in a site support section in one of the data center building slabs at Meta's Rosemount, MN data center project.

Formal tests show that the team exceeded all the technical requirements while achieving good workability and finish performance required for the application.

## Open source for more sustainable construction

At Meta, we believe AI can generate high-performance, low carbon concrete mixes for major construction projects such as data centers. Open source AI can benefit every level of the construction industry, from the construction companies and contractors, to suppliers, providers, architects, and building owners.

The basic AI solution will remain open source to enable further commercial productization, application, and R&D. Our aim is to scale the use of low carbon concrete in data centers and encourage the adoption of performance-based requirements at minimum risk.