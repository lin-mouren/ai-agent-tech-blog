---
title: "Preparing for future AI capabilities in biology"
vendor: openai
source_url: https://openai.com/index/preparing-for-future-ai-capabilities-in-biology/
published_at: 2025-06-18T00:00:00.000Z
crawled_at: 2026-05-23T14:11:22.000Z
word_count: 2280
reading_time_minutes: 12
tags: [ai-safety, biology, biosecurity, preparedness]
---

Preparing for future AI capabilities in biology | OpenAI

June 18, 2025

[Safety](https://openai.com/news/safety-alignment/)

# Preparing for future AI capabilities in biology

As our models grow more capable in biology, we're layering in safeguards and partnering with global experts, including hosting a biodefense summit this July.

Advanced AI models have the power to rapidly accelerate scientific discovery, one of the many ways frontier AI models will benefit humanity. In biology, these models are [already helping scientists](https://www.fiercebiotech.com/medtech/fine-tuned-ai-models-openai-babylon-aim-predict-clinical-trial-successes) identify which new drugs are most likely to succeed in human trials. Soon, they could also accelerate drug discovery, design better vaccines, create enzymes for sustainable fuels, and uncover new treatments for rare diseases to open up new possibilities across medicine, public health, and environmental science.

At the same time, these models raise important dual-use considerations: enabling scientific advancement while maintaining the barrier to harmful information. The same underlying capabilities driving progress, such as reasoning over biological data, predicting chemical reactions, or guiding lab experiments, could also potentially be misused to help people with minimal expertise to recreate biological threats or assist highly skilled actors in creating bioweapons. Physical access to labs and sensitive materials remains a barrier—however those barriers are not absolute.

We expect that upcoming AI models will reach 'High' levels of capability in biology, as measured by our [Preparedness Framework](https://cdn.openai.com/pdf/18a02b5d-6b67-4cec-ab64-68cdfbddebcd/preparedness-framework-v2.pdf), and we're taking a multi-pronged approach to put mitigations in place. In this post, we cover:

- Developing a responsible approach to advancing biological capabilities
- Collaborating with external domain experts including government entities and national labs
- Training models to safely handle dual-use biological requests
- Building detection, monitoring, and enforcement systems
- Adversarial red-teaming our mitigations with experts
- Deploying security controls
- What's ahead

## Our approach

We need to act responsibly amid this uncertainty. That's why we're leaning in on advancing AI integration for positive use cases like biomedical research and biodefense, while at the same time focusing on limiting access to harmful capabilities. Our approach is focused on prevention—we don't think it's acceptable to wait and see whether a bio threat event occurs before deciding on a sufficient level of safeguards.

The future will require deeper expert and government collaboration to strengthen the broader ecosystem and help surface issues that no single organization could catch alone. We've consulted with external experts at every stage of this work. Early on, we worked with leading experts on biosecurity, bioweapons, and bioterrorism, as well as academic researchers, to shape our biosecurity threat model, capability assessments, and model and usage policies. As we designed mitigations, human trainers with master's and PhDs in biology helped create and validate our evaluation data. And now, we're actively engaging with domain-expert red teamers to test how well our safeguards hold up in practice under high fidelity scenarios.

Even as we invest in further research, such as wet lab uplift studies to assess novices' success on harmless proxy tasks, we are preparing and implementing mitigations now. We're also continuing to partner closely with government entities, including the [US CAISI](https://www.nist.gov/aisi) and [UK AISI](https://www.aisi.gov.uk/). We've worked with [Los Alamos National Lab](https://openai.com/index/openai-and-los-alamos-national-laboratory-work-together/) to study AI's role in wet lab settings and support external researchers advancing biosecurity tools and evaluations.

## Strengthening defenses in biology

Over the past two years, we've tracked what our models can do as they develop, worked to reduce risks before launch per the [Preparedness Framework](https://cdn.openai.com/pdf/18a02b5d-6b67-4cec-ab64-68cdfbddebcd/preparedness-framework-v2.pdf), and shared our findings openly through system cards so others can follow our progress.

- **Training the model to refuse or safely respond to harmful requests:** Historically, we've trained models to refuse dangerous requests. For dual use requests (such as virology experiments, immunology, genetic engineering, etc.), we follow the principles outlined in our Model Spec, including avoiding responses that provide actionable steps.
- **Always-on detection systems:** We've deployed robust system-wide monitors across all product surfaces with frontier models to detect risky or suspicious bio-related activity.
- **Monitoring and enforcement checks:** We prohibit use of our products to cause harm, and we enforce our policies when we see misuse.
- **End-to-end red teaming:** We are working with multiple teams of expert red teamers to bypass our defenses end-to-end.
- **Security controls:** We take a defense-in-depth approach to protecting our model weights, relying on a combination of access control, infrastructure hardening, egress controls, and monitoring.

## What's ahead

We're hosting a biodefense summit this July, bringing together a select group of government researchers and NGOs to explore dual-use risks, share progress, and explore how our frontier models can accelerate research.

Building off of our safety work with governments, we believe the public and private sectors should work together to strengthen our society's biological defenses outside of AI models. This could include strengthened nucleic acid synthesis screening, more robust early detection systems for novel pathogens, hardening infrastructure against biothreats, and investing in biosecurity innovations.

We look forward to more collaboration with governments, researchers, and entrepreneurs around the world—not only to ensure that the biosecurity ecosystem is prepared, but to take advantage of the astonishing breakthroughs that are still to come.