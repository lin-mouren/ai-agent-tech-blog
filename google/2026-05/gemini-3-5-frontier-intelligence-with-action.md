---
title: "Gemini 3.5: frontier intelligence with action"
vendor: google
source_url: https://blog.google/innovation-and-ai/models-and-research/gemini-models/gemini-3-5/
published_at: 2026-05-19T17:45:00.000Z
crawled_at: 2026-05-22T06:01:55.172Z
word_count: 1926
reading_time_minutes: 10
tags: [gemini, multimodal, reasoning, safety, agents, infrastructure, evaluation, api, research, product]
---

# Gemini 3.5: frontier intelligence with action

May 19, 2026

·

16 min read

Share

[x.com](https://twitter.com/intent/tweet?text=Gemini%203.5%3A%20frontier%20intelligence%20with%20action%20%40google&url=https://blog.google/innovation-and-ai/models-and-research/gemini-models/gemini-3-5/) [Facebook](https://www.facebook.com/sharer/sharer.php?caption=Gemini%203.5%3A%20frontier%20intelligence%20with%20action&u=https://blog.google/innovation-and-ai/models-and-research/gemini-models/gemini-3-5/) [LinkedIn](https://www.linkedin.com/shareArticle?mini=true&url=https://blog.google/innovation-and-ai/models-and-research/gemini-models/gemini-3-5/&title=Gemini%203.5%3A%20frontier%20intelligence%20with%20action) [Mail](mailto:?subject=Gemini%203.5%3A%20frontier%20intelligence%20with%20action&body=Check%20out%20this%20article%20on%20the%20Keyword:%0A%0AGemini%203.5%3A%20frontier%20intelligence%20with%20action%0A%0AAt%20Google%20I/O%20we%20released%20Gemini%203.5,%20our%20latest%20series%20of%20models%20combining%20frontier%20intelligence%20with%20action.%0A%0Ahttps://blog.google/innovation-and-ai/models-and-research/gemini-models/gemini-3-5/)

Copy link

Gemini 3.5 is built to help you execute complex, agentic workflows.


[![koray](https://storage.googleapis.com/gweb-uniblog-publish-prod/images/koray.max-244x184.format-webp.webp)\\
\\
Koray Kavukcuoglu\\
\\
CTO, Google DeepMind and Chief AI Architect, Google](https://blog.google/authors/koray-kavukcuoglu/) [![Jeff Dean](https://storage.googleapis.com/gweb-uniblog-publish-prod/images/Jeff_Dean_Photo_1.max-244x184.format-webp.webp)\\
\\
Jeff Dean\\
\\
Chief Scientist, Google DeepMind and Google Research](https://blog.google/authors/jeff-dean/)

![oriol_vinyals_bio photo](https://storage.googleapis.com/gweb-uniblog-publish-prod/images/oriol_vinyals_bio_photo.max-244x184.format-webp.webp)

Oriol Vinyals

Vice President, Google DeepMind


![_2709939077_47048311_1300x731](https://storage.googleapis.com/gweb-uniblog-publish-prod/images/_2709939077_47048311_1300x731.max-244x184.format-webp.webp)

Noam Shazeer

Vice President, Google DeepMind


Share

[x.com](https://twitter.com/intent/tweet?text=Gemini%203.5%3A%20frontier%20intelligence%20with%20action%20%40google&url=https://blog.google/innovation-and-ai/models-and-research/gemini-models/gemini-3-5/) [Facebook](https://www.facebook.com/sharer/sharer.php?caption=Gemini%203.5%3A%20frontier%20intelligence%20with%20action&u=https://blog.google/innovation-and-ai/models-and-research/gemini-models/gemini-3-5/) [LinkedIn](https://www.linkedin.com/shareArticle?mini=true&url=https://blog.google/innovation-and-ai/models-and-research/gemini-models/gemini-3-5/&title=Gemini%203.5%3A%20frontier%20intelligence%20with%20action) [Mail](mailto:?subject=Gemini%203.5%3A%20frontier%20intelligence%20with%20action&body=Check%20out%20this%20article%20on%20the%20Keyword:%0A%0AGemini%203.5%3A%20frontier%20intelligence%20with%20action%0A%0AAt%20Google%20I/O%20we%20released%20Gemini%203.5,%20our%20latest%20series%20of%20models%20combining%20frontier%20intelligence%20with%20action.%0A%0Ahttps://blog.google/innovation-and-ai/models-and-research/gemini-models/gemini-3-5/)

Copy link

![Gemini 3.5 text and multi-colored star icon on an abstract blue background.](https://storage.googleapis.com/gweb-uniblog-publish-prod/images/gemini-3-5__keyword__blog-header_.width-200.format-webp.webp)

Today, we’re introducing Gemini 3.5, our latest family of models combining frontier intelligence with action. This represents a major leap forward in building more capable, intelligent agents. We’re kicking off the series by releasing 3.5 Flash. It delivers frontier performance for agents and coding, excelling at complex long-horizon tasks that deliver real-world utility.

3.5 Flash is available today to billions of people globally:

- For everyone via the Gemini app and AI Mode in [Google Search](https://blog.google/products-and-platforms/products/search/search-io-2026)
- For developers in our agent-first development platform Google Antigravity and Gemini API in Google AI Studio and Android Studio
- For enterprises in Gemini Enterprise Agent Platform and Gemini Enterprise.

We’re also hard at work on 3.5 Pro. It's already being used internally, and we look forward to rolling it out next month.

## 3.5 Flash: frontier performance for agents and coding

Gemini 3.5 Flash delivers intelligence that rivals large flagship models on multiple dimensions, at the speeds you have come to expect from the Flash series. It’s our strongest agentic and coding model yet, outperforming Gemini 3.1 Pro on challenging coding and agentic benchmarks like Terminal-Bench 2.1 (76.2%), GDPval-AA (1656 Elo) and MCP Atlas (83.6%), and leading in multimodal understanding (84.2% on CharXiv Reasoning). When looking at output tokens per second, it is 4 times faster than other frontier models.

![Performance comparison table of Gemini, Claude, and GPT models across various benchmarks, highlighting Gemini 3.5 Flash.](https://storage.googleapis.com/gweb-uniblog-publish-prod/original_images/gemini-3-5__benchmarks__light.gif)

Landing in the top-right quadrant of the Artificial Analysis index, 3.5 Flash delivers frontier-level intelligence at exceptional speed — proving you no longer have to trade quality for latency.

[![an image showing "Artificial Analysis Intelligence Index vs Output Speed](https://storage.googleapis.com/gweb-uniblog-publish-prod/images/GeminiModels_Artificial_Analysis_.width-100.format-webp.webp)](https://storage.googleapis.com/gweb-uniblog-publish-prod/images/GeminiModels_Artificial_Analysis_Intelligence_I.original.png)

## 3.5 Flash: agentic tasks at scale

This balance of speed and performance makes 3.5 Flash ideal for tackling long-horizon agentic tasks. What used to take a developer days or an auditor weeks, 3.5 Flash can now help complete in a fraction of the time, often at less than half the cost of other frontier models. It rapidly plans, builds and iterates to solve real-world problems, whether it’s developing new applications, maintaining codebases or helping to prepare financial documents.

When coupled with the updated Antigravity harness, 3.5 Flash becomes a powerful engine for deploying collaborative subagents to tackle problems at scale for the most demanding use cases. Under supervision, it can reliably execute multi-step workflows and coding tasks while sustaining frontier performance.

Sorry, your browser doesn't support embedded videos, but don't worry, you can [download it](https://storage.googleapis.com/gweb-uniblog-publish-prod/original_videos/housecleaning.mp4) and watch it with your favorite video player!

Read more

Powered by Antigravity, 3.5 Flash executes multi-step workflows to automatically rename and categorize unstructured assets based on dynamic criteria.

Sorry, your browser doesn't support embedded videos, but don't worry, you can [download it](https://storage.googleapis.com/gweb-uniblog-publish-prod/original_videos/Compressed_alphazero_demo_658w6BO.mp4) and watch it with your favorite video player!

Read more

Leveraging Antigravity, 3.5 Flash uses two agents to synthesize the AlphaZero paper and code a fully playable game in six hours.

Sorry, your browser doesn't support embedded videos, but don't worry, you can [download it](https://storage.googleapis.com/gweb-uniblog-publish-prod/original_videos/AGY-FLASH35.mp4) and watch it with your favorite video player!

Read more

3.5 Flash uses the Antigravity harness to transform a messy legacy codebase to Next.js.

Sorry, your browser doesn't support embedded videos, but don't worry, you can [download it](https://storage.googleapis.com/gweb-uniblog-publish-prod/original_videos/Compressed_FINAL_AntiGrav_AgenticCities_DZ_v24_1_1_z5UxMwA.mp4) and watch it with your favorite video player!

Read more

3.5 Flash uses subagents to create new city landscapes in Antigravity.

Sorry, your browser doesn't support embedded videos, but don't worry, you can [download it](https://storage.googleapis.com/gweb-uniblog-publish-prod/original_videos/Compressed_FINAL_self-improving-games_yoFcPns.mp4) and watch it with your favorite video player!

Read more

3.5 Flash uses two agents: a builder and a player, working in a rapid self-improvement loop to develop a game in Antigravity.

Jump to position 1Jump to position 2Jump to position 3Jump to position 4Jump to position 5

Building on the strong multimodal foundation of Gemini 3, 3.5 Flash generates richer, more interactive web UIs and graphics.

Sorry, your browser doesn't support embedded videos, but don't worry, you can [download it](https://storage.googleapis.com/gweb-uniblog-publish-prod/original_videos/Compressed_animated-papers_1_1.mp4) and watch it with your favorite video player!

Read more

3.5 Flash creates interactive animations for a research paper on AI Studio.

Sorry, your browser doesn't support embedded videos, but don't worry, you can [download it](https://storage.googleapis.com/gweb-uniblog-publish-prod/original_videos/Compressed_animated_html_1.mp4) and watch it with your favorite video player!

Read more

3.5 Flash turns a plain text description into interactive hardware on AI Studio.

Sorry, your browser doesn't support embedded videos, but don't worry, you can [download it](https://storage.googleapis.com/gweb-uniblog-publish-prod/original_videos/Compressed_FINAL_gemini_brandAgents_260518c_1_LPpucSO.mp4) and watch it with your favorite video player!

Read more

3.5 Flash executes multiple concepts in parallel to build a full branding concept for a school fundraiser on AI Studio.

Sorry, your browser doesn't support embedded videos, but don't worry, you can [download it](https://storage.googleapis.com/gweb-uniblog-publish-prod/original_videos/Compressed_FINAL_Payments_UI_04_1.mp4) and watch it with your favorite video player!

Read more

3.5 Flash generates different UX approaches for a checkout flow in just 60 seconds on AI Studio.

Jump to position 1Jump to position 2Jump to position 3Jump to position 4

## 3.5 Flash: real-world impact

3.5 Flash’s real-world agentic capabilities are already driving meaningful progress for our developers and enterprises alike. In developing the 3.5 model series, we worked closely with industry partners to understand where toil and complexity arose in their workflows. Partners are seeing meaningful impact — from banks and fintechs automating multi-week workflows to data science teams unearthing insights amidst complex data environments.

![YouTube video for shopify](https://i.ytimg.com/vi_webp/zdY0QaI1paI/default.webp)

00:00

Read more

Shopify is running subagents in parallel to analyze complex data over a long horizon for more accurate merchant growth forecasts at a global scale.

![YouTube video showing macquarie bank](https://i.ytimg.com/vi_webp/CLxFAk5SvB8/default.webp)

00:00

Read more

Macquarie Bank is piloting how 3.5 Flash can accelerate customer onboarding by reasoning over complex 100+ page documents, retrieving relevant information and making reliable recommendations with low latency.

![YouTube video for salesforce](https://i.ytimg.com/vi_webp/9qfJzcq_ZOg/default.webp)

00:00

Read more

Salesforce is integrating 3.5 Flash into Agentforce to reliably automate complicated enterprise tasks by deploying multiple subagents that retain context and execute complex, multi-turn tool calling.

![YouTube video for ramp](https://i.ytimg.com/vi_webp/LrrR8OZTrbA/default.webp)

00:00

Read more

3.5 Flash is helping Ramp enable smarter, more reliable OCR through multimodal understanding of complex invoices combined with reasoning over historical patterns.

![YouTube video for xero](https://i.ytimg.com/vi_webp/0WKFm_t-Nk4/default.webp)

00:00

Read more

Xero is deploying agents to autonomously manage complex, multi-week workflows, such as identifying suppliers and gathering information for 1099 tax forms, enabling small businesses to automate tedious admin tasks.

![YouTube video for databricks](https://i.ytimg.com/vi_webp/fskhwriwEh0/default.webp)

00:00

Read more

Databricks is using agentic workflows to monitor and retrieve real-time information, reason across massive datasets to diagnose issues, identify fixes and propose solutions for data scientists.

Jump to position 1Jump to position 2Jump to position 3Jump to position 4Jump to position 5Jump to position 6

## Personal AI agents: built with 3.5 Flash

3.5 Flash is now the default model for the Gemini app and AI Mode in Search globally. At I/O today, we showed how its agentic capabilities are powering new features to bring frontier-level intelligence to your daily life.

The new Gemini Spark, your personal AI agent, uses 3.5 Flash. It runs 24/7, helping you navigate your digital life, taking action on your behalf while under your direction. We’re starting to roll out Gemini Spark to trusted testers today, and we’re planning on bringing the Beta to Google AI Ultra subscribers in the US next week.

![an image of Gemini Spark](https://storage.googleapis.com/gweb-uniblog-publish-prod/images/Spark_-_1.width-100.format-webp.webp)

Gemini Spark uses 3.5 Flash to help accomplish these tasks

![an image of Gemini Spark](https://storage.googleapis.com/gweb-uniblog-publish-prod/images/Spark_-_2.width-100.format-webp.webp)

Gemini Spark uses 3.5 Flash to help accomplish these tasks

![an image of Gemini Spark](https://storage.googleapis.com/gweb-uniblog-publish-prod/images/Spark_-_3.width-100.format-webp.webp)

Gemini Spark uses 3.5 Flash to help accomplish these tasks

![an image of Gemini Spark](https://storage.googleapis.com/gweb-uniblog-publish-prod/images/Spark_-_4.width-100.format-webp.webp)

Gemini Spark uses 3.5 Flash to help accomplish these tasks

![an image of Gemini Spark](https://storage.googleapis.com/gweb-uniblog-publish-prod/images/Spark_-_5.width-100.format-webp.webp)

Gemini Spark uses 3.5 Flash to help accomplish these tasks

Jump to position 1Jump to position 2Jump to position 3Jump to position 4Jump to position 5

The enhanced agentic coding capabilities of 3.5 Flash are also delivering even more intelligent experiences across Search, from introducing new information agents that work for you 24/7 to unlocking more dynamic generative UI experiences. [Learn more in our blog post](https://blog.google/products-and-platforms/products/search/search-io-2026).

Sorry, your browser doesn't support embedded videos, but don't worry, you can [download it](https://storage.googleapis.com/gweb-uniblog-publish-prod/original_videos/AIM-GenWidgets_Gyro_1920x1080_small_16D0pmZ.mp4) and watch it with your favorite video player!

Search leverages 3.5 Flash to build an interactive visual explaining Gyroid patterns.

## Gemini 3.5: built with frontier safeguards

Gemini 3.5 was developed in accordance with our Frontier Safety Framework. We have strengthened our cyber and CBRN safeguards, which means it's less likely to generate harmful content, and to mistakenly refuse to answer safe queries. We achieve this with new, more advanced safety training and mitigations, including [interpretability tools](https://arxiv.org/abs/2601.11516v4) that help check and understand the AI's inner reasoning before it provides a response.

## 3.5 Flash is available today

Gemini 3.5 Flash is generally available via Google Antigravity, the Gemini API in Google AI Studio and Android Studio, [Gemini Enterprise Agent Platform](https://console.cloud.google.com/agent-platform/overview) and [Gemini Enterprise](https://cloud.google.com/gemini-enterprise?e=48754805). It’s also now available to everyone in the Gemini app and AI Mode in Search. On behalf of the entire Gemini team, we can’t wait to see what you build.

[Collection\\
\\
![The image shows a colorful abstract design with the Google I/O 2026 logo.](https://storage.googleapis.com/gweb-uniblog-publish-prod/images/IOCollection_social.width-600.format-webp.webp)\\
\\
**I/O 2026** \\
\\
Here’s a look at everything we announced at Google I/O 2026.\\
\\
See more](https://blog.google/innovation-and-ai/technology/developers-tools/google-io-2026-collection/)

![](https://blog.google/static/blogv2/images/newsletter-envelope-back.svg?version=pr20260507-1819)

![](https://blog.google/static/blogv2/images/newsletter-envelope-letter-approved.svg?version=pr20260507-1819)

![](https://blog.google/static/blogv2/images/newsletter-envelope-letter-google.svg?version=pr20260507-1819)

![](https://blog.google/static/blogv2/images/newsletter-envelope-front.svg?version=pr20260507-1819)

## Get more stories from Google in your inbox.Get more stories from Google in your inbox.

Email address


Your information will be used in accordance with
[Google's privacy policy.](https://policies.google.com/privacy)

Subscribe


Done. Just one step more.


Check your inbox to confirm your subscription.


You are already subscribed to our newsletter.

You can also subscribe with a
different email address
.


POSTED IN:

### Related stories

[![](https://storage.googleapis.com/gweb-uniblog-publish-prod/images/MissouriSocial.width-300.format-webp.webp)\\
\\
Global Network **We’re announcing new community investments in Missouri.**\\
\\
May 20, 2026](https://blog.google/innovation-and-ai/infrastructure-and-cloud/global-network/missouri-programs/)

[![](https://storage.googleapis.com/gweb-uniblog-publish-prod/images/100_things_Social.width-300.format-webp.webp)\\
\\
AI **100 things we announced at I/O 2026**\\
\\
By\\
\\
\\
\\
Keyword Team\\
\\
\\
May 20, 2026](https://blog.google/innovation-and-ai/technology/ai/google-io-2026-all-our-announcements/)

[![](https://storage.googleapis.com/gweb-uniblog-publish-prod/images/Screenshot_2026-05-15_at_4.21.29P.width-300.format-webp.webp)\\
\\
Google Research **A new experiment brings better group meetings to Google Beam**\\
\\
By\\
\\
\\
\\
Mohamed Abdelgany\\
\\
\\
May 20, 2026](https://blog.google/innovation-and-ai/models-and-research/google-research/google-beam-group-meetings/)

[![](https://storage.googleapis.com/gweb-uniblog-publish-prod/images/AI_Mode_US.width-300.format-webp.webp)\\
\\
Search **How AI Mode is changing the way people search in the U.S.**\\
\\
By\\
\\
\\
\\
Shivani Mohan\\
\\
\\
May 19, 2026](https://blog.google/products-and-platforms/products/search/ai-mode-us-insights/)

[![](https://storage.googleapis.com/gweb-uniblog-publish-prod/images/GoogleWorkspace-IO.width-300.format-webp.webp)\\
\\
Google Workspace **New ways to create and get things done in Google Workspace**\\
\\
By\\
\\
\\
\\
Yulie Kwon Kim\\
\\
\\
May 19, 2026](https://blog.google/products-and-platforms/products/workspace/workspace-updates/)

[![](https://storage.googleapis.com/gweb-uniblog-publish-prod/images/GeminiOmni_social.width-300.format-webp.webp)\\
\\
Gemini models **Introducing Gemini Omni**\\
\\
By\\
\\
\\
\\
Koray Kavukcuoglu](https://blog.google/innovation-and-ai/models-and-research/gemini-models/gemini-omni/)

.

Jump to position 1
Jump to position 2
Jump to position 3
Jump to position 4
Jump to position 5
Jump to position 6

![](https://blog.google/static/blogv2/images/newsletter_toast.svg?version=pr20260507-1819)

Let’s stay in touch. Get the latest news from Google in your inbox.

[Subscribe](https://blog.google/newsletter-subscribe/) No thanks

Survey

Help us improve The Keyword with a one-question survey

YesNo

This survey is anonymous. All responses will be aggregated and used only for analysis to improve our services.

Did this article provide the level of detail you were looking for?

Yes, I got what I neededNo, I wanted more technical depthNo, I wanted a simpler overviewI was looking for something else entirely

✅

Thank you!