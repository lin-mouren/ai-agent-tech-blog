---
title: "From Brain Waves to Words: Brain2Qwerty Offers a New Path to Communication Without Surgery"
vendor: meta
source_url: https://ai.meta.com/blog/brain2qwerty-brain-ai-human-communication/
published_at: 2026-06-29T13:00:07.089Z
crawled_at: 2026-06-30T02:00:48.788Z
word_count: 660
reading_time_minutes: 4
tags: [llama, agents, infrastructure, research, product, open-source]
---

[Go up one level](https://ai.meta.com/blog/brain2qwerty-brain-ai-human-communication/# "Go up one level") [](https://ai.meta.com/)

- [Products](https://ai.meta.com/blog/brain2qwerty-brain-ai-human-communication/#)

- [AI Research](https://ai.meta.com/blog/brain2qwerty-brain-ai-human-communication/#)

- [Resources](https://ai.meta.com/blog/brain2qwerty-brain-ai-human-communication/#)

- [About](https://ai.meta.com/blog/brain2qwerty-brain-ai-human-communication/#)

- [Get Llama](https://www.llama.com/?utm_source=ai_meta_site&utm_medium=web&utm_content=AI_nav&utm_campaign=09252025_moment)


- [Try Meta AI](https://applink.meta.ai/?utm_source=ai_meta_site&utm_medium=web&utm_content=AI_nav&utm_campaign=04082026_moment)
- [Toggle site search](https://ai.meta.com/blog/brain2qwerty-brain-ai-human-communication/# "Toggle site search")


[Close submenu](https://ai.meta.com/blog/brain2qwerty-brain-ai-human-communication/# "Close submenu") [Main menu](https://ai.meta.com/blog/brain2qwerty-brain-ai-human-communication/# "Main menu")

[BACK](https://ai.meta.com/blog/brain2qwerty-brain-ai-human-communication/# "Go up one level")

- [Meta AI](https://ai.meta.com/meta-ai/)
- [Vibes](https://ai.meta.com/vibes/)
- [AI Studio](https://ai.meta.com/ai-studio/)

- [Overview](https://ai.meta.com/research/)
- [Projects](https://ai.meta.com/research/#projects)
- [Research Areas](https://ai.meta.com/research/#research-areas)
- [People](https://ai.meta.com/results/?content_types[0]=person)

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
>](https://ai.meta.com/blog/brain2qwerty-brain-ai-human-communication/#)

- [AI Research\\
\\
>](https://ai.meta.com/blog/brain2qwerty-brain-ai-human-communication/#)

- [Resources\\
\\
>](https://ai.meta.com/blog/brain2qwerty-brain-ai-human-communication/#)

- [About\\
\\
>](https://ai.meta.com/blog/brain2qwerty-brain-ai-human-communication/#)

- [Get Llama](https://www.llama.com/?utm_source=ai_meta_site&utm_medium=web&utm_content=AI_nav&utm_campaign=09252025_moment)

[Try Meta AI](https://applink.meta.ai/?utm_source=ai_meta_site&utm_medium=web&utm_content=AI_nav&utm_campaign=04082026_moment)

Research

# From Brain Waves to Words: Brain2Qwerty Offers a New Path to Communication Without Surgery

June 29, 2026•

3 minute read

Last year, we introduced [Brain2Qwerty](https://ai.meta.com/blog/brain-ai-research-human-communication/) v1, research that uses AI to decode brain activity into text without any surgical implant. Now we're sharing the next step: Brain2Qwerty v2, the highest-performing end-to-end pipeline capable of real-time sentence decoding from non-invasive brain recordings, approaching levels of accuracy previously exclusive to techniques that require brain surgery.

To help accelerate neuroscience breakthroughs, we're releasing the full training code for Brain2Qwerty v1 and v2, and our partner, the Basque Center on Cognition, Brain, and Language (BCBL), is releasing the [v1 dataset](https://huggingface.co/datasets/bcbl190626/SpanishBCBL). We believe this research has the potential to make a real difference for the [millions of people](https://thejns.org/view/journals/j-neurosurg/130/4/article-p1080.xml) who suffer from brain lesions that prevent them from communicating. Invasive procedures like stereotactic electroencephalography and electrocorticography have shown that a neuroprosthesis feeding signals to an AI decoder can restore communication, but they're difficult to scale. Our noninvasive approach can help bridge that gap.



We trained Brain2Qwerty v2 on approximately 22,000 sentences from nine volunteer participants, each recorded for 10 hours wearing a magnetoencephalography (MEG) device while actively typing. Instead of relying on hand-crafted pipelines to detect neural events, we use end-to-end deep learning to decode directly from raw brain signals.



Fine-tuning large language models on neural data allows the system to leverage semantic context, bridging the gap between noisy brain recordings and coherent language. We also deployed AI agents to explore optimizations for the decoding pipeline, with final training configurations selected manually by engineers.



The result: Brain2Qwerty v2 recovers sentences coherently from noisy neural inputs, achieving a word accuracy rate of 61%, significantly improving upon the 8% word accuracy from [other non-invasive methods](https://www.nature.com/articles/s41593-023-01304-9)). And for our best participant, we achieve a 78% word accuracy, where more than half of all sentences are decoded with one word error or less.

We also find that decoding accuracy improves log-linearly with data volume, suggesting that the remaining performance gap with surgical approaches could be further narrowed through data scaling alone. This work contributes to our efforts to build open foundational models of the brain, with our [Tribev2 model](https://ai.meta.com/blog/tribe-v2-brain-predictive-foundation-model/) for perception encoding, [NeuralSet](https://arxiv.org/html/2605.03169v1) to process brain data at scale, and [NeuralBench](https://arxiv.org/abs/2605.08495) to systematically evaluate models. We do this in close collaboration with the community, through our recent $5 million fund to stimulate open datasets in our [Digital Brain Project](https://digitalbrainproject.org/). Our hope is that this work, done in the open, advances neuroscience to identify, diagnose, and treat neurological disorders faster than in siloes.

[Read the Brain2Qwerty v2 Paper](https://ai.meta.com/research/publications/accurate-decoding-of-natural-sentences-from-non-invasive-brain-recordings/)

[Download the Code](https://github.com/facebookresearch/brain2qwerty)

[Download the Data](https://huggingface.co/datasets/bcbl190626/SpanishBCBL)

[Read the Brain2Qwerty v1 Blog](https://ai.meta.com/blog/brain-ai-research-human-communication/)

[Read about Brain2Qwerty in Nature Neuroscience](https://www.nature.com/articles/s41593-026-02303-2)

[Our approach](https://ai.meta.com/about)

[About AI at Meta](https://ai.meta.com/about)

[People](https://ai.meta.com/results/?content_types%5B0%5D=person&sort_by=random)

[Careers](https://www.metacareers.com/jobs/?is_leadership=0&sub_teams[0]=Artificial%20Intelligence&is_in_page=0)

[Research](https://ai.meta.com/research)

[Infrastructure](https://ai.meta.com/infrastructure)

[Resources](https://ai.meta.com/resources)

[Demos](https://aidemos.meta.com/)

[Meta AI](https://ai.meta.com/meta-ai/)

[Explore Meta AI](https://ai.meta.com/meta-ai/)

[Get Meta AI](https://ai.meta.com/get-meta-ai/)

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

[Meta AI](https://ai.meta.com/meta-ai/) [Explore Meta AI](https://ai.meta.com/meta-ai/) [Get Meta AI](https://ai.meta.com/get-meta-ai/) [AI Studio](https://ai.meta.com/ai-studio/)

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