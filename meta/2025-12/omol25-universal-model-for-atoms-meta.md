---
title: "OMol25 and Universal Model for Atoms: World's Largest Molecular DFT Dataset"
date: 2025-12-16
vendor: meta
tags: [FAIR, molecular-science, chemistry, dataset, computational-chemistry, open-source, OMol25, UMA]
source: https://ai.meta.com/blog/meta-fair-science-new-open-source-releases
---

# OMol25 and Universal Model for Atoms: World's Largest Molecular DFT Dataset

**Date:** May 14, 2025 (initial) / December 2025 (expanded 500TB release)  
**Vendor:** Meta (FAIR Chemistry Team + Lawrence Berkeley National Laboratory)  
**Source:** https://ai.meta.com/blog/meta-fair-science-new-open-source-releases

## Overview

Meta FAIR released Open Molecules 2025 (OMol25), the world's largest and most diverse dataset of high-accuracy quantum chemistry calculations, along with Meta's Universal Model for Atoms (UMA). These tools accelerate molecular and materials discovery with unprecedented scale and accuracy.

## OMol25 Dataset

- **Scale:** 83 million unique molecular systems, 100+ million DFT calculations, 6+ billion CPU core-hours
- **10-100x larger** than previous state-of-the-art molecular datasets (SPICE, AIMNet2)
- **Coverage:** Biomolecules, metal complexes, electrolytes, small molecules, systems up to 350 atoms
- **Method:** Hybrid DFT calculations using ORCA v6.0.1 quantum chemistry software
- **Partners:** Meta FAIR + Lawrence Berkeley National Laboratory
- **Expanded Release (Dec 2025):** ~500 TB with raw DFT outputs, electronic densities, wavefunctions, molecular orbital information for 4M+ high-accuracy quantum chemical calculations (via Argonne ALCF partnership)

## Universal Model for Atoms (UMA)

- Machine learning interatomic potential trained on 30+ billion atoms
- Unifies OMol25 with other Meta FAIR chemistry datasets
- Provides more accurate predictions of molecular behavior across diverse chemical systems
- Particularly strong at predicting forces, energies, and molecular dynamics

## Research Impact

Expected to drive years of innovation in:
- Drug discovery (protein-ligand binding)
- Battery electrolyte optimization
- Catalyst design
- Materials science

Dataset creation at this scale is now the foundation for next-generation physics-informed ML models.

## Resources

- Blog: https://ai.meta.com/blog/meta-fair-science-new-open-source-releases
- ArXiv: https://arxiv.org/abs/2505.08762
- HuggingFace: https://huggingface.co/facebook/OMol25
