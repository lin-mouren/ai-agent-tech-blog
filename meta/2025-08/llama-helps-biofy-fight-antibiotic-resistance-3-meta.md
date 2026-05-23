---
title: "How Llama helps Biofy Technologies in the fight against antibiotic resistance"
vendor: meta
source_url: https://ai.meta.com/blog/llama-helps-biofy-fight-antibiotic-resistance/
published_at: 2025-08-07T00:00:00.000Z
crawled_at: 2026-05-23T14:29:11.000Z
word_count: 620
reading_time_minutes: 4
tags: [llama, healthcare, ai-for-science, open-source]
---

# How Llama helps Biofy Technologies in the fight against antibiotic resistance

August 7, 2025

Antibiotic resistance poses a significant threat to global health and is a common cause of death in hospitals. To address this challenge in their home country of Brazil, the biotech company Biofy Technologies has developed a groundbreaking platform using Llama that reduces diagnostic time for antibiotic resistance from five days to less than four hours.

Biofy developed a system to identify bacteria and their antibiotic resistance using a vector database and pieces of bacterial DNA. To do that, the Biofy team customized the Llama 3.2 90B model to work with the original genome database and generate new synthetic DNA samples. The result was Biofy's Abby Recommender.

The solution runs on Oracle Cloud Infrastructure (OCI) and dedicated GPUs. Abby Recommender can analyze DNA, identify bacteria, and recommend the correct antibiotic to use based on bacteria resistance.

"A platform that can rapidly identify antibiotic-resistant bacteria and propose effective treatment can save lives," says Biofy CEO Paulo Perez. "Llama is a fundamental component used to create the genome vector database for our solution. We chose it because it is open source, fully customizable, and suited to the problem we needed to solve."

Biofy uses Llama with OCI Generative AI and Oracle AI Vector Search. The team developed a proprietary model to convert DNA using Oracle Autonomous 23ai Database with Vector DB. Biofy's algorithms check whether a genome is valid and stable for bacterial DNA, then test the synthetic data created by the Llama 3.2 90B model.