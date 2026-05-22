---
title: "Scaling How We Build and Test Our Most Advanced AI"
vendor: meta
source_url: https://ai.meta.com/blog/scaling-how-we-build-test-advanced-ai/
published_at: 2026-04-08T00:00:00.000Z
crawled_at: 2026-05-22T06:01:55.193Z
word_count: 1120
reading_time_minutes: 6
tags: [llama, reasoning, safety, agents, api, product, open-source]
---

[Go up one level](https://ai.meta.com/blog/scaling-how-we-build-test-advanced-ai/# "Go up one level") [![Meta](https://scontent-lax3-1.xx.fbcdn.net/v/t39.8562-6/252294889_575082167077436_6034106545912333281_n.svg/meta-logo-primary_standardsize.svg?_nc_cat=108&ccb=1-7&_nc_sid=e280be&_nc_ohc=b4qWJDeoQe8Q7kNvwFFmyPS&_nc_oc=AdoLJF628k9gts4pDAyBmzCugA1pB69GwZqJUdjGz_3mLeuXw68rZr5ZE0S1x-qnPPY&_nc_zt=14&_nc_ht=scontent-lax3-1.xx&_nc_gid=DYDmBlcvorJCvK8oMUGgMw&_nc_ss=7b289&oh=00_Af48oNqGQsrFunV1QgTJxafZQEGTwpcFFK-FNzDuLzd26w&oe=6A15CEF9)](https://ai.meta.com/)

- [Products](https://ai.meta.com/blog/scaling-how-we-build-test-advanced-ai/#)

- [AI Research](https://ai.meta.com/blog/scaling-how-we-build-test-advanced-ai/#)

- [Resources](https://ai.meta.com/blog/scaling-how-we-build-test-advanced-ai/#)

- [About](https://ai.meta.com/blog/scaling-how-we-build-test-advanced-ai/#)

- [Get Llama](https://www.llama.com/?utm_source=ai_meta_site&utm_medium=web&utm_content=AI_nav&utm_campaign=09252025_moment)


- [Try Meta AI](https://applink.meta.ai/?utm_source=ai_meta_site&utm_medium=web&utm_content=AI_nav&utm_campaign=04082026_moment)
- [Toggle site search](https://ai.meta.com/blog/scaling-how-we-build-test-advanced-ai/# "Toggle site search")


[Close submenu](https://ai.meta.com/blog/scaling-how-we-build-test-advanced-ai/# "Close submenu") [Main menu](https://ai.meta.com/blog/scaling-how-we-build-test-advanced-ai/# "Main menu")

[BACK](https://ai.meta.com/blog/scaling-how-we-build-test-advanced-ai/# "Go up one level")

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
>](https://ai.meta.com/blog/scaling-how-we-build-test-advanced-ai/#)

- [AI Research\\
\\
>](https://ai.meta.com/blog/scaling-how-we-build-test-advanced-ai/#)

- [Resources\\
\\
>](https://ai.meta.com/blog/scaling-how-we-build-test-advanced-ai/#)

- [About\\
\\
>](https://ai.meta.com/blog/scaling-how-we-build-test-advanced-ai/#)

- [Get Llama](https://www.llama.com/?utm_source=ai_meta_site&utm_medium=web&utm_content=AI_nav&utm_campaign=09252025_moment)

[Try Meta AI](https://applink.meta.ai/?utm_source=ai_meta_site&utm_medium=web&utm_content=AI_nav&utm_campaign=04082026_moment)

FEATURED

# Scaling How We Build and Test Our Most Advanced AI

April 8, 2026•

8 minute read

![](https://scontent-lax3-2.xx.fbcdn.net/v/t39.2365-6/666078108_26263986099896647_5092766563902137193_n.png?_nc_cat=106&ccb=1-7&_nc_sid=e280be&_nc_ohc=QeAK3w-ojAMQ7kNvwE48kWC&_nc_oc=Ado5stAq-XXJk5lGrE_73n7IxkNSDk9qmM151IJKYlLGLKVzVQdHJO6WFMPZGSCZqGs&_nc_zt=14&_nc_ht=scontent-lax3-2.xx&_nc_gid=DYDmBlcvorJCvK8oMUGgMw&_nc_ss=7b289&oh=00_Af6l0G0P-mFt5SZ9lyDh-X4P5KPU7U93sBRQRyMGISG7uw&oe=6A2A4161)

As we build more capable and more personalized AI, reliability, security, and user protections are more important than ever.

Advanced models require an advanced approach to safety — one that scales with the technology. Today, we’re detailing that work: our updated [Advanced AI Scaling Framework](https://ai.meta.com/static-resource/Meta_Advanced-AI-Scaling-Framework-v2), our [Safety & Preparedness Report](https://ai.meta.com/static-resource/muse-spark-safety-and-preparedness-report/) for Muse Spark, and new advances in how our models reason about safety from the ground up, so that as our AI becomes more capable, our protections keep pace.

### Advanced AI Scaling Framework

Today, we’re building on our original Frontier AI Framework and publishing a significantly updated and more rigorous version: the Advanced AI Scaling Framework. This update broadens the types of risks we evaluate, strengthens how we make deployment decisions, and introduces new Safety & Preparedness Reports. More specifically, this Framework outlines how we identify and assess the most severe and emerging risks, including chemical and biological, cybersecurity, and a new section to evaluate risks around loss of control. As models become more advanced, we’re evaluating how they perform when given greater autonomy and whether the controls around that behavior work as intended. These standards apply across our frontier deployments, whether they’re open, controlled API access, or closed models.

In practice, this also means mapping potential risks, evaluating models before and after safeguards are applied to confirm they work in the real world, and only deploying models when they meet the standards set by our Framework. For people who use Meta AI across our apps, this means the models powering their experience have been evaluated across a broad spectrum of risks before we make them available.

While our updated Framework strengthens the standards and safeguards for our most capable models, our new Safety & Preparedness Reports will show how we are meeting them. These reports will detail our risk assessments, evaluation results, the rationale behind our deployment decisions, and any limitations we’re still working to address. This transparency means we will share what we found, how we tested our models, where our evaluations fell short, and how we closed those gaps.

### Safety & Preparedness Report

For Muse Spark, we conducted extensive safety evaluations before deployment. Because of its advanced reasoning capabilities, we evaluated the model before and after applying protections — testing not just for the most serious risks like cybersecurity and chemical and biological threats, but also against our long-standing safety policies, which are designed to prevent harms and misuse like violence, child safety violations, and criminal wrongdoing, and our policies to ensure ideological balance.

Our evaluation approach is multilayered by design, and it starts before a model is deployed. We test against thousands of scenarios specifically designed to find weaknesses, track how often those attempts succeed, and work to drive that number as low as possible. Because no evaluation is exhaustive, we also monitor live traffic with automated systems designed to spot unexpected issues so we can address them quickly. The results demonstrate strong safeguards across all the risk categories we measured. Our evaluations also showed that Muse Spark is at the frontier in avoiding ideological bias in model responses.

We also evaluated whether the model could act autonomously in ways that could be difficult to control, and our evaluations confirm it does not possess the level of autonomous capability needed to pose those risks. Our Safety & Preparedness Report details the specific evaluations behind this finding in addition to all of our evaluation results, including what we tested and what we found.

### Safety That Scales With the Model

These protections are built in at every stage — from filtering the data the model learns from, to safety-focused training, to guardrails that run at the product level. And because our protections need to evolve as the sophistication of our models improves, this work will never be done.

In particular, Muse Spark is more capable than our previous generation of models, and that capability is what makes a fundamentally new approach to governing the model possible. Earlier approaches relied on teaching models to handle specific scenarios one by one, for instance, training them to refuse to respond or to redirect to a trusted source. That approach worked, but was difficult to scale. Because Muse Spark can reason, we’ve evolved our approach: we’ve translated our trust and safety guidelines across areas like content and conversational safety, response quality, and handling different viewpoints into clear, testable principles. We also trained the model on why something is safe — not just on the rules, but also the reasons behind the rules. This means the model is better equipped to handle novel situations that rules-based systems might have failed to anticipate.

This work doesn’t replace human oversight; it elevates it. Our teams design the principles that guide model behavior, rigorously validate these principles against real-world scenarios, and layer in additional guardrails to catch things the model may still miss. The result is protections that are applied more broadly and consistently, and that improve as the model’s reasoning improves.

## Showing Our Work

As we make significant advancements to Meta AI and deploy our most capable models, our Safety & Preparedness Reports show how we’re evaluating and managing risk at every step. We’ll continue to invest in safeguards, testing, and research, so people can rely on an AI experience with built-in protections designed to help keep them safe.

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

![](https://scontent-lax3-2.xx.fbcdn.net/v/t39.2365-6/87524316_2677189655726266_6338721200264445952_n.svg?_nc_cat=103&ccb=1-7&_nc_sid=e280be&_nc_ohc=Z8DNIEuKF1YQ7kNvwG9-4v4&_nc_oc=AdpREi9Fg6pSi1m7Kh0NRg-PHFxkNAxFWfNBBFp7DirQBuuRX2IWhJTU01rSdiJZmh8&_nc_zt=14&_nc_ht=scontent-lax3-2.xx&_nc_gid=DYDmBlcvorJCvK8oMUGgMw&_nc_ss=7b289&oh=00_Af6Jw7glGFYwG_XPDKh3EvJkc9L3DrJp_8u2M1ve1YyE5w&oe=6A2A38B8)

![](https://scontent-lax3-2.xx.fbcdn.net/v/t39.2365-6/85559716_2814260008668824_1992323131183726592_n.svg?_nc_cat=103&ccb=1-7&_nc_sid=e280be&_nc_ohc=mTCVkVFt0eEQ7kNvwEnSeML&_nc_oc=AdrkVNMjkxgUtoaW4yVp9HT3ismkCeP-yduj4tLlbYjmJD_OwV1m-R9oKd8Gp9Kj2rc&_nc_zt=14&_nc_ht=scontent-lax3-2.xx&_nc_gid=DYDmBlcvorJCvK8oMUGgMw&_nc_ss=7b289&oh=00_Af7uAxX9Q3vqpG7_Xg7T_oFY-WZVfrAqXwVde4bJZOErjQ&oe=6A2A3D8F)

[![](https://scontent-lax3-2.xx.fbcdn.net/v/t39.8562-6/335682312_964107378293184_3093631164486164913_n.svg?_nc_cat=100&ccb=1-7&_nc_sid=e280be&_nc_ohc=1cYY7wB0lfEQ7kNvwHkXjG-&_nc_oc=AdplQ4MFdXwMu_owx33a9h3MQHdv61HldsovMZ8114_UVvg0LuXD8J4db7t5neREQY0&_nc_zt=14&_nc_ht=scontent-lax3-2.xx&_nc_gid=DYDmBlcvorJCvK8oMUGgMw&_nc_ss=7b289&oh=00_Af5-Z2jNAFMxyA_QWAH2N-bPzFVeEW9BtrCo6KC38HyBHw&oe=6A15BF27)\\
\\
![](https://scontent-lax3-2.xx.fbcdn.net/v/t39.8562-6/335682312_964107378293184_3093631164486164913_n.svg?_nc_cat=100&ccb=1-7&_nc_sid=e280be&_nc_ohc=1cYY7wB0lfEQ7kNvwHkXjG-&_nc_oc=AdplQ4MFdXwMu_owx33a9h3MQHdv61HldsovMZ8114_UVvg0LuXD8J4db7t5neREQY0&_nc_zt=14&_nc_ht=scontent-lax3-2.xx&_nc_gid=DYDmBlcvorJCvK8oMUGgMw&_nc_ss=7b289&oh=00_Af5-Z2jNAFMxyA_QWAH2N-bPzFVeEW9BtrCo6KC38HyBHw&oe=6A15BF27)](https://www.facebook.com/aiatmeta/)

[![](https://scontent-lax3-2.xx.fbcdn.net/v/t39.8562-6/336009607_1870102080040414_6753977241281150924_n.svg?_nc_cat=103&ccb=1-7&_nc_sid=e280be&_nc_ohc=Y0YUrpUMRnIQ7kNvwHcvpL-&_nc_oc=AdpWmlz8yPyxqn33SLYxcxX6EDpTLrvwVnJAyXUEY7ixRrFCvrPnD0reANWsPuFNYDY&_nc_zt=14&_nc_ht=scontent-lax3-2.xx&_nc_gid=DYDmBlcvorJCvK8oMUGgMw&_nc_ss=7b289&oh=00_Af4Xd-cXsNeBcrTEPsRJJgg7U2Ov2s4roWTl5VYg1GPIfw&oe=6A15B762)\\
\\
![](https://scontent-lax3-2.xx.fbcdn.net/v/t39.8562-6/336009607_1870102080040414_6753977241281150924_n.svg?_nc_cat=103&ccb=1-7&_nc_sid=e280be&_nc_ohc=Y0YUrpUMRnIQ7kNvwHcvpL-&_nc_oc=AdpWmlz8yPyxqn33SLYxcxX6EDpTLrvwVnJAyXUEY7ixRrFCvrPnD0reANWsPuFNYDY&_nc_zt=14&_nc_ht=scontent-lax3-2.xx&_nc_gid=DYDmBlcvorJCvK8oMUGgMw&_nc_ss=7b289&oh=00_Af4Xd-cXsNeBcrTEPsRJJgg7U2Ov2s4roWTl5VYg1GPIfw&oe=6A15B762)](https://twitter.com/aiatmeta/)

[![](https://scontent-lax3-1.xx.fbcdn.net/v/t39.8562-6/336289415_1541032296405649_2165099305308791297_n.svg?_nc_cat=109&ccb=1-7&_nc_sid=e280be&_nc_ohc=8bounfEuaS4Q7kNvwGGoUke&_nc_oc=AdrbnaPCAfNxgL3YAoHBkIeglQ_d7rhjVA7zLWOfOKfzluO72UBGVYnlS2vH5ehhpi0&_nc_zt=14&_nc_ht=scontent-lax3-1.xx&_nc_gid=DYDmBlcvorJCvK8oMUGgMw&_nc_ss=7b289&oh=00_Af6yQxj80r-BgDBDMP9gF443gcdVQ5EuNZT9h0HvBtNasA&oe=6A15AAFB)\\
\\
![](https://scontent-lax3-1.xx.fbcdn.net/v/t39.8562-6/336289415_1541032296405649_2165099305308791297_n.svg?_nc_cat=109&ccb=1-7&_nc_sid=e280be&_nc_ohc=8bounfEuaS4Q7kNvwGGoUke&_nc_oc=AdrbnaPCAfNxgL3YAoHBkIeglQ_d7rhjVA7zLWOfOKfzluO72UBGVYnlS2vH5ehhpi0&_nc_zt=14&_nc_ht=scontent-lax3-1.xx&_nc_gid=DYDmBlcvorJCvK8oMUGgMw&_nc_ss=7b289&oh=00_Af6yQxj80r-BgDBDMP9gF443gcdVQ5EuNZT9h0HvBtNasA&oe=6A15AAFB)](https://www.linkedin.com/showcase/aiatmeta)

[![](https://scontent-lax3-1.xx.fbcdn.net/v/t39.8562-6/335648731_142576991793348_7786819189843639239_n.svg?_nc_cat=108&ccb=1-7&_nc_sid=e280be&_nc_ohc=ZflYyZAnRdIQ7kNvwEcehdQ&_nc_oc=Adr6AS3Q8HPnL5vEDM7CLtQcHfmNvbT2tSUK9mWaY6dWHdD9ytvUyqTZhel7xfCrEC0&_nc_zt=14&_nc_ht=scontent-lax3-1.xx&_nc_gid=DYDmBlcvorJCvK8oMUGgMw&_nc_ss=7b289&oh=00_Af61R5OKalgb-wW_F3nxZ2DS36AF5bN1-IBx9QCvZWO2ow&oe=6A15C46E)\\
\\
![](https://scontent-lax3-1.xx.fbcdn.net/v/t39.8562-6/335648731_142576991793348_7786819189843639239_n.svg?_nc_cat=108&ccb=1-7&_nc_sid=e280be&_nc_ohc=ZflYyZAnRdIQ7kNvwEcehdQ&_nc_oc=Adr6AS3Q8HPnL5vEDM7CLtQcHfmNvbT2tSUK9mWaY6dWHdD9ytvUyqTZhel7xfCrEC0&_nc_zt=14&_nc_ht=scontent-lax3-1.xx&_nc_gid=DYDmBlcvorJCvK8oMUGgMw&_nc_ss=7b289&oh=00_Af61R5OKalgb-wW_F3nxZ2DS36AF5bN1-IBx9QCvZWO2ow&oe=6A15C46E)](https://www.youtube.com/@aiatmeta)

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

[![](https://scontent-lax3-2.xx.fbcdn.net/v/t39.8562-6/335682312_964107378293184_3093631164486164913_n.svg?_nc_cat=100&ccb=1-7&_nc_sid=e280be&_nc_ohc=1cYY7wB0lfEQ7kNvwHkXjG-&_nc_oc=AdplQ4MFdXwMu_owx33a9h3MQHdv61HldsovMZ8114_UVvg0LuXD8J4db7t5neREQY0&_nc_zt=14&_nc_ht=scontent-lax3-2.xx&_nc_gid=DYDmBlcvorJCvK8oMUGgMw&_nc_ss=7b289&oh=00_Af5-Z2jNAFMxyA_QWAH2N-bPzFVeEW9BtrCo6KC38HyBHw&oe=6A15BF27)\\
\\
![](https://scontent-lax3-2.xx.fbcdn.net/v/t39.8562-6/335682312_964107378293184_3093631164486164913_n.svg?_nc_cat=100&ccb=1-7&_nc_sid=e280be&_nc_ohc=1cYY7wB0lfEQ7kNvwHkXjG-&_nc_oc=AdplQ4MFdXwMu_owx33a9h3MQHdv61HldsovMZ8114_UVvg0LuXD8J4db7t5neREQY0&_nc_zt=14&_nc_ht=scontent-lax3-2.xx&_nc_gid=DYDmBlcvorJCvK8oMUGgMw&_nc_ss=7b289&oh=00_Af5-Z2jNAFMxyA_QWAH2N-bPzFVeEW9BtrCo6KC38HyBHw&oe=6A15BF27)](https://www.facebook.com/aiatmeta/)

[![](https://scontent-lax3-2.xx.fbcdn.net/v/t39.8562-6/336009607_1870102080040414_6753977241281150924_n.svg?_nc_cat=103&ccb=1-7&_nc_sid=e280be&_nc_ohc=Y0YUrpUMRnIQ7kNvwHcvpL-&_nc_oc=AdpWmlz8yPyxqn33SLYxcxX6EDpTLrvwVnJAyXUEY7ixRrFCvrPnD0reANWsPuFNYDY&_nc_zt=14&_nc_ht=scontent-lax3-2.xx&_nc_gid=DYDmBlcvorJCvK8oMUGgMw&_nc_ss=7b289&oh=00_Af4Xd-cXsNeBcrTEPsRJJgg7U2Ov2s4roWTl5VYg1GPIfw&oe=6A15B762)\\
\\
![](https://scontent-lax3-2.xx.fbcdn.net/v/t39.8562-6/336009607_1870102080040414_6753977241281150924_n.svg?_nc_cat=103&ccb=1-7&_nc_sid=e280be&_nc_ohc=Y0YUrpUMRnIQ7kNvwHcvpL-&_nc_oc=AdpWmlz8yPyxqn33SLYxcxX6EDpTLrvwVnJAyXUEY7ixRrFCvrPnD0reANWsPuFNYDY&_nc_zt=14&_nc_ht=scontent-lax3-2.xx&_nc_gid=DYDmBlcvorJCvK8oMUGgMw&_nc_ss=7b289&oh=00_Af4Xd-cXsNeBcrTEPsRJJgg7U2Ov2s4roWTl5VYg1GPIfw&oe=6A15B762)](https://twitter.com/aiatmeta/)

[![](https://scontent-lax3-1.xx.fbcdn.net/v/t39.8562-6/336289415_1541032296405649_2165099305308791297_n.svg?_nc_cat=109&ccb=1-7&_nc_sid=e280be&_nc_ohc=8bounfEuaS4Q7kNvwGGoUke&_nc_oc=AdrbnaPCAfNxgL3YAoHBkIeglQ_d7rhjVA7zLWOfOKfzluO72UBGVYnlS2vH5ehhpi0&_nc_zt=14&_nc_ht=scontent-lax3-1.xx&_nc_gid=DYDmBlcvorJCvK8oMUGgMw&_nc_ss=7b289&oh=00_Af6yQxj80r-BgDBDMP9gF443gcdVQ5EuNZT9h0HvBtNasA&oe=6A15AAFB)\\
\\
![](https://scontent-lax3-1.xx.fbcdn.net/v/t39.8562-6/336289415_1541032296405649_2165099305308791297_n.svg?_nc_cat=109&ccb=1-7&_nc_sid=e280be&_nc_ohc=8bounfEuaS4Q7kNvwGGoUke&_nc_oc=AdrbnaPCAfNxgL3YAoHBkIeglQ_d7rhjVA7zLWOfOKfzluO72UBGVYnlS2vH5ehhpi0&_nc_zt=14&_nc_ht=scontent-lax3-1.xx&_nc_gid=DYDmBlcvorJCvK8oMUGgMw&_nc_ss=7b289&oh=00_Af6yQxj80r-BgDBDMP9gF443gcdVQ5EuNZT9h0HvBtNasA&oe=6A15AAFB)](https://www.linkedin.com/showcase/aiatmeta)

[![](https://scontent-lax3-1.xx.fbcdn.net/v/t39.8562-6/335648731_142576991793348_7786819189843639239_n.svg?_nc_cat=108&ccb=1-7&_nc_sid=e280be&_nc_ohc=ZflYyZAnRdIQ7kNvwEcehdQ&_nc_oc=Adr6AS3Q8HPnL5vEDM7CLtQcHfmNvbT2tSUK9mWaY6dWHdD9ytvUyqTZhel7xfCrEC0&_nc_zt=14&_nc_ht=scontent-lax3-1.xx&_nc_gid=DYDmBlcvorJCvK8oMUGgMw&_nc_ss=7b289&oh=00_Af61R5OKalgb-wW_F3nxZ2DS36AF5bN1-IBx9QCvZWO2ow&oe=6A15C46E)\\
\\
![](https://scontent-lax3-1.xx.fbcdn.net/v/t39.8562-6/335648731_142576991793348_7786819189843639239_n.svg?_nc_cat=108&ccb=1-7&_nc_sid=e280be&_nc_ohc=ZflYyZAnRdIQ7kNvwEcehdQ&_nc_oc=Adr6AS3Q8HPnL5vEDM7CLtQcHfmNvbT2tSUK9mWaY6dWHdD9ytvUyqTZhel7xfCrEC0&_nc_zt=14&_nc_ht=scontent-lax3-1.xx&_nc_gid=DYDmBlcvorJCvK8oMUGgMw&_nc_ss=7b289&oh=00_Af61R5OKalgb-wW_F3nxZ2DS36AF5bN1-IBx9QCvZWO2ow&oe=6A15C46E)](https://www.youtube.com/@aiatmeta)

[Privacy Policy](https://www.facebook.com/about/privacy/)

[Terms](https://www.facebook.com/policies/)

[Cookies](https://www.facebook.com/policies/cookies/)

Meta © 2026

[![](https://scontent-lax3-2.xx.fbcdn.net/v/t39.8562-6/335682312_964107378293184_3093631164486164913_n.svg?_nc_cat=100&ccb=1-7&_nc_sid=e280be&_nc_ohc=1cYY7wB0lfEQ7kNvwHkXjG-&_nc_oc=AdplQ4MFdXwMu_owx33a9h3MQHdv61HldsovMZ8114_UVvg0LuXD8J4db7t5neREQY0&_nc_zt=14&_nc_ht=scontent-lax3-2.xx&_nc_gid=DYDmBlcvorJCvK8oMUGgMw&_nc_ss=7b289&oh=00_Af5-Z2jNAFMxyA_QWAH2N-bPzFVeEW9BtrCo6KC38HyBHw&oe=6A15BF27)\\
\\
![](https://scontent-lax3-2.xx.fbcdn.net/v/t39.8562-6/335682312_964107378293184_3093631164486164913_n.svg?_nc_cat=100&ccb=1-7&_nc_sid=e280be&_nc_ohc=1cYY7wB0lfEQ7kNvwHkXjG-&_nc_oc=AdplQ4MFdXwMu_owx33a9h3MQHdv61HldsovMZ8114_UVvg0LuXD8J4db7t5neREQY0&_nc_zt=14&_nc_ht=scontent-lax3-2.xx&_nc_gid=DYDmBlcvorJCvK8oMUGgMw&_nc_ss=7b289&oh=00_Af5-Z2jNAFMxyA_QWAH2N-bPzFVeEW9BtrCo6KC38HyBHw&oe=6A15BF27)](https://www.facebook.com/aiatmeta/)

[![](https://scontent-lax3-2.xx.fbcdn.net/v/t39.8562-6/336009607_1870102080040414_6753977241281150924_n.svg?_nc_cat=103&ccb=1-7&_nc_sid=e280be&_nc_ohc=Y0YUrpUMRnIQ7kNvwHcvpL-&_nc_oc=AdpWmlz8yPyxqn33SLYxcxX6EDpTLrvwVnJAyXUEY7ixRrFCvrPnD0reANWsPuFNYDY&_nc_zt=14&_nc_ht=scontent-lax3-2.xx&_nc_gid=DYDmBlcvorJCvK8oMUGgMw&_nc_ss=7b289&oh=00_Af4Xd-cXsNeBcrTEPsRJJgg7U2Ov2s4roWTl5VYg1GPIfw&oe=6A15B762)\\
\\
![](https://scontent-lax3-2.xx.fbcdn.net/v/t39.8562-6/336009607_1870102080040414_6753977241281150924_n.svg?_nc_cat=103&ccb=1-7&_nc_sid=e280be&_nc_ohc=Y0YUrpUMRnIQ7kNvwHcvpL-&_nc_oc=AdpWmlz8yPyxqn33SLYxcxX6EDpTLrvwVnJAyXUEY7ixRrFCvrPnD0reANWsPuFNYDY&_nc_zt=14&_nc_ht=scontent-lax3-2.xx&_nc_gid=DYDmBlcvorJCvK8oMUGgMw&_nc_ss=7b289&oh=00_Af4Xd-cXsNeBcrTEPsRJJgg7U2Ov2s4roWTl5VYg1GPIfw&oe=6A15B762)](https://twitter.com/aiatmeta/)

[![](https://scontent-lax3-1.xx.fbcdn.net/v/t39.8562-6/336289415_1541032296405649_2165099305308791297_n.svg?_nc_cat=109&ccb=1-7&_nc_sid=e280be&_nc_ohc=8bounfEuaS4Q7kNvwGGoUke&_nc_oc=AdrbnaPCAfNxgL3YAoHBkIeglQ_d7rhjVA7zLWOfOKfzluO72UBGVYnlS2vH5ehhpi0&_nc_zt=14&_nc_ht=scontent-lax3-1.xx&_nc_gid=DYDmBlcvorJCvK8oMUGgMw&_nc_ss=7b289&oh=00_Af6yQxj80r-BgDBDMP9gF443gcdVQ5EuNZT9h0HvBtNasA&oe=6A15AAFB)\\
\\
![](https://scontent-lax3-1.xx.fbcdn.net/v/t39.8562-6/336289415_1541032296405649_2165099305308791297_n.svg?_nc_cat=109&ccb=1-7&_nc_sid=e280be&_nc_ohc=8bounfEuaS4Q7kNvwGGoUke&_nc_oc=AdrbnaPCAfNxgL3YAoHBkIeglQ_d7rhjVA7zLWOfOKfzluO72UBGVYnlS2vH5ehhpi0&_nc_zt=14&_nc_ht=scontent-lax3-1.xx&_nc_gid=DYDmBlcvorJCvK8oMUGgMw&_nc_ss=7b289&oh=00_Af6yQxj80r-BgDBDMP9gF443gcdVQ5EuNZT9h0HvBtNasA&oe=6A15AAFB)](https://www.linkedin.com/showcase/aiatmeta)

[![](https://scontent-lax3-1.xx.fbcdn.net/v/t39.8562-6/335648731_142576991793348_7786819189843639239_n.svg?_nc_cat=108&ccb=1-7&_nc_sid=e280be&_nc_ohc=ZflYyZAnRdIQ7kNvwEcehdQ&_nc_oc=Adr6AS3Q8HPnL5vEDM7CLtQcHfmNvbT2tSUK9mWaY6dWHdD9ytvUyqTZhel7xfCrEC0&_nc_zt=14&_nc_ht=scontent-lax3-1.xx&_nc_gid=DYDmBlcvorJCvK8oMUGgMw&_nc_ss=7b289&oh=00_Af61R5OKalgb-wW_F3nxZ2DS36AF5bN1-IBx9QCvZWO2ow&oe=6A15C46E)\\
\\
![](https://scontent-lax3-1.xx.fbcdn.net/v/t39.8562-6/335648731_142576991793348_7786819189843639239_n.svg?_nc_cat=108&ccb=1-7&_nc_sid=e280be&_nc_ohc=ZflYyZAnRdIQ7kNvwEcehdQ&_nc_oc=Adr6AS3Q8HPnL5vEDM7CLtQcHfmNvbT2tSUK9mWaY6dWHdD9ytvUyqTZhel7xfCrEC0&_nc_zt=14&_nc_ht=scontent-lax3-1.xx&_nc_gid=DYDmBlcvorJCvK8oMUGgMw&_nc_ss=7b289&oh=00_Af61R5OKalgb-wW_F3nxZ2DS36AF5bN1-IBx9QCvZWO2ow&oe=6A15C46E)](https://www.youtube.com/@aiatmeta)

Facebook