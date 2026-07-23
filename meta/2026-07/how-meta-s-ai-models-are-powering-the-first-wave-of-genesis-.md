---
title: "How Meta’s AI Models Are Powering the First Wave of Genesis Mission Projects"
vendor: meta
source_url: https://ai.meta.com/blog/genesis-mission-lawrence-berkeley-national-laboratory-segment-anything-dino/
published_at: 2026-07-22T02:00:06.201Z
crawled_at: 2026-07-23T02:00:33.312Z
word_count: 1297
reading_time_minutes: 7
tags: [llama, multimodal, agents, infrastructure, api, product, open-source]
---

[Go up one level](https://ai.meta.com/blog/genesis-mission-lawrence-berkeley-national-laboratory-segment-anything-dino/# "Go up one level") [](https://ai.meta.com/)

- [Products](https://ai.meta.com/blog/genesis-mission-lawrence-berkeley-national-laboratory-segment-anything-dino/#)

- [AI Research](https://ai.meta.com/blog/genesis-mission-lawrence-berkeley-national-laboratory-segment-anything-dino/#)

- [Resources](https://ai.meta.com/blog/genesis-mission-lawrence-berkeley-national-laboratory-segment-anything-dino/#)

- [About](https://ai.meta.com/blog/genesis-mission-lawrence-berkeley-national-laboratory-segment-anything-dino/#)

- [Meta Model API](https://developer.meta.com/ai/)


- [Try Meta AI](https://applink.meta.ai/?pt=10684&pid=ai_meta_site&utm_source=ai_meta_site&utm_medium=web&utm_campaign=nav_try-meta-ai-palette_07072026&utm_content=nav_try-meta-ai-palette_07072026&ct=nav_try-meta-ai-palette_07072026&referrer=utm_source%3Dai_meta_site%26utm_medium%3Dweb%26utm_campaign%3Dnav_try-meta-ai-palette_07072026%26utm_content%3Dnav_try-meta-ai-palette_07072026)
- [Toggle site search](https://ai.meta.com/blog/genesis-mission-lawrence-berkeley-national-laboratory-segment-anything-dino/# "Toggle site search")


[Close submenu](https://ai.meta.com/blog/genesis-mission-lawrence-berkeley-national-laboratory-segment-anything-dino/# "Close submenu") [Main menu](https://ai.meta.com/blog/genesis-mission-lawrence-berkeley-national-laboratory-segment-anything-dino/# "Main menu")

[BACK](https://ai.meta.com/blog/genesis-mission-lawrence-berkeley-national-laboratory-segment-anything-dino/# "Go up one level")

- [Meta AI](https://ai.meta.com/meta-ai/assistant/)
- [Media Generation](https://ai.meta.com/meta-ai/media-generation/)
- [Vibes](https://ai.meta.com/meta-ai/vibes/)
- [AI Studio](https://ai.meta.com/ai-studio/)

- [Overview](https://ai.meta.com/research/)
- [Projects](https://ai.meta.com/research/#projects)
- [Resources & Tools](https://ai.meta.com/resources/)
- [Publications](https://ai.meta.com/results/?content_types[0]=publication)
- [GitHub](https://github.com/facebookresearch/)

- [Blog](https://ai.meta.com/blog/)
- [Learning Hub](https://ai.meta.com/learn/)
- [Demos](https://aidemos.meta.com/)

- [Overview](https://ai.meta.com/about/)
- [Open Source](https://ai.meta.com/opensourceai/)
- [Careers](https://www.metacareers.com/)

Clear

- Clear

- [Products\\
\\
>](https://ai.meta.com/blog/genesis-mission-lawrence-berkeley-national-laboratory-segment-anything-dino/#)

- [AI Research\\
\\
>](https://ai.meta.com/blog/genesis-mission-lawrence-berkeley-national-laboratory-segment-anything-dino/#)

- [Resources\\
\\
>](https://ai.meta.com/blog/genesis-mission-lawrence-berkeley-national-laboratory-segment-anything-dino/#)

- [About\\
\\
>](https://ai.meta.com/blog/genesis-mission-lawrence-berkeley-national-laboratory-segment-anything-dino/#)

- [Meta Model API](https://developer.meta.com/ai/)

[Try Meta AI](https://applink.meta.ai/?pt=10684&pid=ai_meta_site&utm_source=ai_meta_site&utm_medium=web&utm_campaign=nav_try-meta-ai-palette_07072026&utm_content=nav_try-meta-ai-palette_07072026&ct=nav_try-meta-ai-palette_07072026&referrer=utm_source%3Dai_meta_site%26utm_medium%3Dweb%26utm_campaign%3Dnav_try-meta-ai-palette_07072026%26utm_content%3Dnav_try-meta-ai-palette_07072026)

Open Source

# How Meta’s AI Models Are Powering the First Wave of Genesis Mission Projects

July 21, 2026•

6 minute read



[Lawrence Berkeley National Laboratory](https://www.lbl.gov/) — one of the [US Department of Energy's](https://www.energy.gov/) premier research laboratories, known for Nobel Prize-winning work in physics, chemistry, and materials science — operates some of the most advanced scientific facilities on the planet. Among them is the [Advanced Light Source](https://als.lbl.gov/) (ALS), a football field-sized facility that produces intensely bright beams of X-ray light, allowing researchers to study materials from the atomic and molecular scale all the way to plants. The ALS's instruments, known as beamlines, generate enormous quantities of data — and as recent facility upgrades have dramatically increased their resolution and speed, the volume of data has exploded beyond what scientists can keep up with.

The numbers are staggering: The DOE's light and neutron source facilities now produce tens of petabytes of data annually — that's millions of gigabytes, roughly equivalent to streaming 2 million hours of HD video. This backlog didn't always exist. Upgraded detectors, which have gone from capturing a single image every six seconds to 100,000 images per second, mean these facilities now generate orders of magnitude more data than they did a decade ago, and traditional manual analysis simply can't keep pace.

The problem goes beyond volume: domain experts are scarce and overwhelmed, and modern in-situ experiments — where scientists observe dynamic processes like chemical reactions or material failures as they occur — demand real-time interpretation that no human team can deliver manually.

Much of the analysis challenge comes down to one task: segmentation — the process of identifying and drawing precise boundaries around distinct structures within an image. In computer vision, segmentation is what enables everything from medical scans that distinguish tumors from healthy tissue to autonomous vehicles that separate pedestrians from pavement. In scientific research, segmentation is what transforms a raw X-ray image from a wall of grayscale pixels into a labeled map of meaningful structures — cell walls, mineral grains, semiconductor layers — that researchers can quantify and compare across experiments.

## SYNAPS-I and the Genesis Mission

In late 2025, the White House launched [The Genesis Mission](https://www.energy.gov/undersecretaryforscience/genesis-mission/genesis-mission), a sweeping national initiative to accelerate scientific discovery and technological leadership using advanced artificial intelligence, led by DOE. SYNAPS-I (SYnergistic Neutron And Photon Science – Intelligence) is one of its flagship projects: a multi-lab initiative led by Berkeley Lab, in partnership with [Argonne](https://www.anl.gov/), [Brookhaven](https://www.bnl.gov/world/), [Oak Ridge](https://www.ornl.gov/), and [SLAC](https://www6.slac.stanford.edu/) National Laboratories, aimed at transforming data analysis across X-ray and neutron science from a months-long bottleneck into a real-time discovery engine, with scientific imaging as a major target. Nowhere is that bottleneck more acute than in image segmentation, where extracting meaningful structures from experimental data can consume weeks of expert effort per dataset.

At the heart of SYNAPS-I's segmentation pipeline are two open-source foundation models released by Meta: [Segment Anything Model 3](https://ai.meta.com/research/sam3/) (SAM 3) and [DINOv3](https://ai.meta.com/research/dinov3/).

## How SAM and DINO Transform Scientific Imaging

DINOv3 is a self-supervised vision model, meaning it learns visual patterns from raw images without requiring humans to label them first. It excels at understanding what different structures in an image represent and where they are located. SAM takes that understanding a step further, drawing precise boundaries around individual objects in an image — much like a scientist carefully outlining structures by hand, but in seconds rather than hours.

Together, the two models form a complementary pipeline: SAM delivers precise, pixel-level boundaries, while DINO provides global context to identify each structure and its place within the sample. The SYNAPS-I team fine-tuned both models on scientific imaging data collected at DOE beamlines, then deployed them across 300 A100 GPUs — the high-performance computing chips that power today's most advanced AI systems — at national supercomputing facilities such as [NERSC](https://www.nersc.gov/). The result: a fully reconstructed, semantically labeled 3D volume delivered back to the scientist physically standing at the beamline instrument, ready for interpretation while the experiment is still running. Total turnaround: approximately 15 minutes.

## Real-World Impact: Understanding Drought Resilience in Grapevines

The SYNAPS-I team demonstrated this pipeline on a pressing agricultural challenge — understanding how grapevines respond to drought at the cellular level. Using micro-CT scans collected at the Advanced Light Source, the pipeline reconstructs 3D volumes of vine stems and automatically identifies xylem vessels — the microscopic tubes responsible for water transport within the plant. By tracking how these vessels change as drought progresses, researchers gain insights that could inform the development of drought-resilient crops, and provide solutions for agricultural resilience into the future.



Micro-CT scan of a grapevine stem, segmented by SYNAPS-I. Cyan: hydrated xylem vessels; dark purple: dry.

What previously required a month of expert annotation per time step now takes 15 minutes, enabling scientists to study dynamic biological processes at the speed of data acquisition itself.

## Why Open Source Matters

National laboratories keep prepublication research data and AI models on government infrastructure, not external cloud services. This work must be managed on secure platforms while in progress. Meta's open source approach makes this possible. The SYNAPS-I team can download, fine-tune, and deploy SAM and DINO within their own secure computing environments, adapting models originally trained on natural images to scientific domains they were never designed for.

With 60 researchers across five national labs, SYNAPS-I is building toward a future where user facilities operate as intelligent discovery platforms — where AI doesn't just process data faster, but helps scientists generate hypotheses, recommends next experiments, and transfers knowledge across facilities so that a breakthrough at one beamline benefits researchers at all of them. As Genesis scales from seed projects to full programs, that open source foundation is poised to accelerate discovery across an expanding set of national priorities.

At the recent Trillion Parameter Consortium, DOE Under Secretary Dario Gil referred to the promise of this effort.

"By seamlessly combining AI, advanced computing, and experimental systems, SYNAPS-I analyzes data as it's produced and guides experiments in real time, replacing slow manual steps with adaptive, automated decision-making," he said. "This compresses discovery time from days to moments and establishes a continuous, self-improving model of science that will be essential to realizing the full potential of the Genesis Mission."

[Learn More About DINOv3](https://ai.meta.com/research/dinov3/)

[Learn More About SAM 3](https://ai.meta.com/research/sam3/)

Our latest updates delivered to your inbox

[Subscribe](https://ai.facebook.com/subscribe/) to our newsletter to keep up with Meta AI news, events, research breakthroughs, and more.

## Join us in the pursuit of what’s possible with AI.

[See all open positions](https://www.metacareers.com/jobs/?is_leadership=0&sub_teams%5B0%5D=Artificial+Intelligence&is_in_page=0&fbclid=IwAR0O8BF7opOj5gASJmwYVGalPPXTLu-6xrl9w00eC7Rarp2HQ9uEH8tERFw)

[Our approach](https://ai.meta.com/about)

[About AI at Meta](https://ai.meta.com/about)

[People](https://ai.meta.com/results/?content_types%5B0%5D=person&sort_by=random)

[Careers](https://www.metacareers.com/jobs/?is_leadership=0&sub_teams[0]=Artificial%20Intelligence&is_in_page=0)

[Research](https://ai.meta.com/research)

[Infrastructure](https://ai.meta.com/infrastructure)

[Resources](https://ai.meta.com/resources)

[Demos](https://aidemos.meta.com/)

[Meta AI](https://ai.meta.com/meta-ai/)

[Assistant](https://ai.meta.com/meta-ai/assistant/)

[Media Generation](https://ai.meta.com/meta-ai/media-generation/)

[Vibes](https://ai.meta.com/meta-ai/vibes/)

[AI Studio](https://ai.meta.com/ai-studio/)

[Latest news](https://ai.meta.com/blog)

[Blog](https://ai.meta.com/blog)

[Newsletter](https://ai.meta.com/subscribe)

Foundational models

[Llama](https://www.llama.com/)





[\\
\\
](https://www.facebook.com/aiatmeta/)

[\\
\\
](https://twitter.com/aiatmeta/)

[\\
\\
](https://www.linkedin.com/showcase/aiatmeta)

[\\
\\
](https://www.youtube.com/@aiatmeta)

Our approach

[Our approach](https://ai.meta.com/about) [About AI at Meta](https://ai.meta.com/about) [People](https://ai.meta.com/results/?content_types%5B0%5D=person&sort_by=random) [Careers](https://www.metacareers.com/jobs/?is_leadership=0&sub_teams[0]=Artificial%20Intelligence&is_in_page=0)

Research

[Research](https://ai.meta.com/research) [Infrastructure](https://ai.meta.com/infrastructure) [Resources](https://ai.meta.com/resources) [Demos](https://aidemos.meta.com/)

Meta AI

[Meta AI](https://ai.meta.com/meta-ai/) [Assistant](https://ai.meta.com/meta-ai/assistant/) [Media Generation](https://ai.meta.com/meta-ai/media-generation/) [Vibes](https://ai.meta.com/meta-ai/vibes/) [AI Studio](https://ai.meta.com/ai-studio/)

Latest news

[Latest news](https://ai.meta.com/blog) [Blog](https://ai.meta.com/blog) [Newsletter](https://ai.meta.com/subscribe)

Foundational models

[Llama](https://www.llama.com/)

[\\
\\
](https://www.facebook.com/aiatmeta/)

[\\
\\
](https://twitter.com/aiatmeta/)

[\\
\\
](https://www.linkedin.com/showcase/aiatmeta)

[\\
\\
](https://www.youtube.com/@aiatmeta)

[Privacy Policy](https://www.facebook.com/about/privacy/)

[Terms](https://www.facebook.com/policies/)

[Cookies](https://www.facebook.com/policies/cookies/)

Meta © 2026

[\\
\\
](https://www.facebook.com/aiatmeta/)

[\\
\\
](https://twitter.com/aiatmeta/)

[\\
\\
](https://www.linkedin.com/showcase/aiatmeta)

[\\
\\
](https://www.youtube.com/@aiatmeta)

Facebook

Facebook

Facebook

Facebook