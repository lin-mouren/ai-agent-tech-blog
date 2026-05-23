---
title: "Measuring AI's capability to accelerate biological research in the wet lab"
vendor: openai
source_url: https://openai.com/index/accelerating-biological-research-in-the-wet-lab/
published_at: 2025-12-16T00:00:00.000Z
crawled_at: 2026-05-23T14:59:27.000Z
word_count: 3500
reading_time_minutes: 18
tags: [research, biology, science, gpt-5, wet-lab]
---

# Measuring AI's capability to accelerate biological research in the wet lab

December 16, 2025

GPT-5 created novel wet lab protocol improvements, optimizing the efficiency of a molecular cloning protocol by 79x.

Accelerating scientific progress is one of the most valuable ways AI can benefit humanity. With GPT-5, we're beginning to see early signs of this—not only in helping researchers move faster through the scientific literature, but also in supporting new forms of scientific reasoning.

Progress to date has been most visible in fields like mathematics, theoretical physics, and theoretical computer science. Biology is different: most advances depend on experimental execution, iteration, and empirical validation in the laboratory.

To help understand how frontier models behave in these settings, we worked with Red Queen Bio, a biosecurity start-up, to build an evaluation framework that tests how a model proposes, analyzes, and iterates on ideas in the wet lab. We set up a simple molecular biology experimental system and had GPT-5 optimize a molecular cloning protocol for efficiency.

Over multiple rounds of experimentation, GPT-5 introduced a novel mechanism that improved cloning efficiency by 79x. Cloning is a fundamental molecular biology tool. The efficiency of cloning methods is critical for creating large, complex libraries central to protein engineering, genetic screens, and organismal strain engineering.

### Experimental results

In this set-up, GPT-5 autonomously reasoned about the cloning protocol, proposed modifications, and incorporated data from new experiments to suggest more improvements. The only human intervention was having scientists carry out the modified protocol and upload experimental data.

Over the course of multiple rounds, GPT-5 optimized the cloning procedure to improve the efficiency by over 79x—meaning that for a fixed amount of input DNA, we recovered 79x more sequence-verified clones than the baseline protocol. Most notably, it introduced two enzymes that constitute a novel mechanism: the recombinase RecA from E. coli, and phage T4 gene 32 single-stranded DNA-binding protein (gp32). Working in tandem, gp32 smooths and detangles the loose DNA ends, and RecA then guides each strand to its correct match.

### A novel improvement to homology-based cloning

GPT-5 proposed a new enzymatic procedure, which the model called RecA-Assisted Pair-and-Finish HiFi Assembly (RAPF-HiFi), that adds two new proteins to the reaction: the recombinase RecA from E. coli, and the phage T4 gene 32 single-stranded DNA-binding protein (gp32). Further, the model made deliberate modifications to the incubation temperature and time, and the timing of enzymatic additions.

On the transformation side, the most effective modification proved unexpectedly simple: pelleting the cells, removing half of the supplied volume, and resuspending the cells before adding DNA, all at 4°C.

### The future

We believe that these experiments offer a snapshot of what future AI-accelerated science will look like: models continually learning and interacting with the real world. Although our experiments excluded human intervention to purely measure model capabilities, we're particularly excited about AI helping human scientists design experiments and contribute to research breakthroughs.