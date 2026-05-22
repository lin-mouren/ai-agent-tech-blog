---
title: "How Physicists Are Using AI to Chase New Physics - Blog | OpenAI Academy"
vendor: openai
source_url: https://academy.openai.com/en/public/blogs/how-physicists-are-using-ai-to-chase-new-physics-2026-03-25
published_at: 2026-03-25T17:41:05.000Z
crawled_at: 2026-05-22T06:01:55.108Z
word_count: 878
reading_time_minutes: 5
tags: [gpt, reasoning, agents, infrastructure, api, research]
---

Article

March 25, 2026

# How Physicists Are Using AI to Chase New Physics

![How Physicists Are Using AI to Chase New Physics](https://cdn.gradual.com/images/https://d2xo500swnpgl1.cloudfront.net/uploads/oaiacademy/Screenshot-2026-03-25-at-10-40-15-AM-5fb43c11-4e9f-44ea-a828-df436c435604-1774460432696.jpeg?fit=scale-down&width=400)

\# physics

\# science

## At UC Santa Barbara and KITP, researchers built an agent-based system with OpenAI models and collider software to compress weeks of theoretical physics work into minutes.

[Share via email](mailto:?subject=%5BOpenAI%20Academy%5D%20How%20Physicists%20Are%20Using%20AI%20to%20Chase%20New%20Physics&body=https%3A%2F%2Facademy.openai.com%2Fpublic%2Fblogs%2Fhow-physicists-are-using-ai-to-chase-new-physics-2026-03-25)

![How Physicists Are Using AI to Chase New Physics](https://cdn.gradual.com/images/https://d2xo500swnpgl1.cloudfront.net/uploads/oaiacademy/Screenshot-2026-03-25-at-10-40-15-AM-5fb43c11-4e9f-44ea-a828-df436c435604-1774460432696.jpeg?fit=scale-down&width=400)

A small team of physicists at UC Santa Barbara and the [Kavli Institute for Theoretical Physics](https://www.linkedin.com/company/kavli-institute-for-theoretical-physics/) is using OpenAI models in the hopes of speeding up the search for a new physics.

[Amalia Madden](https://www.linkedin.com/in/amalia-madden-233b08168/), a post-doc at KITP, began using AI as if it were a colleague. At first it was just useful in small ways, clarifying a question when she was confused, or needed help bridging the gap to another discipline. Back then, she says, it felt like talking to a very well-read student. Slowly models improved until she and UCSB PhD candidate [Inigo Valenzuela Lombera](https://www.linkedin.com/in/inigo-v-1074a7235/) realized they could use reasoning models for a much harder problem: building and testing explanations for unexplained data coming out of particle colliders.

Physicists jokingly call that “ambulance chasing.” A collider experiment throws out a deviation from the so-called Standard Model, the theory explaining most fundamental particles and forces in physics. Theorists rush in to explain anomalies, propose new particles or interactions, code up their hypothesis, run it through simulation software, and check whether the idea can reproduce the signal without conflicting with everything else that is known.

Before AI, that process could consume weeks of graduate-student time. OpenAI models helped Madden and Valenzuela Lombera, along with professors [Nathanial Craig](https://www.linkedin.com/in/nathaniel-craig-532356360/) and [Prateek Agrawal](https://www.linkedin.com/in/prateek-agrawal-3a875979/) of UCSB and post-doc Jessica Howard of KITP, compress that cycle to minutes with a system called [FERMIACC, a closed-loop agent pipeline](https://arxiv.org/abs/2603.22538) built with the OpenAI Agents SDK and combined with familiar collider tools like FeynRules, MadGraph and Pythia. Hypothesis generation can take seconds, and a full pass through fast simulation and collider analysis can finish in under ten minutes.

A well-known incident in 2015 shows why this matters. That year, the Large Hadron Collider surfaced a surprising excess resonance in the data. It hinted at a new boson, and roughly 500 papers followed. But in the end, the effect disappeared: a false alarm that cost years of human effort in total.

FERMIACC is designed to resolve such readings fast. With FERMIACC, agents propose models, generate events, compare simulated signatures with observed data, and score the result, with deterministic checks on how particles are supposed to interact and decay.

Madden and Valenzuela Lombera noted there were limits, in physics, to what they could accomplish with AI in the browser. In ChatGPT, a model can be a clever collaborator and a strong algebra checker. But through the API, with structured outputs, tool calls, and agents passing state to one another, it begins to serve as scientific infrastructure. Build in a coding environment with Codex, connect the model to software researchers already trust, and vet the results with verifiers.

They see collider data as the first use case among many. The same tools could help read cosmological data, where faint signatures from cosmic inflation, dark matter, and the early universe may point the way to epiphanies.

![Ads No.5. Click to open https://edunewsletter.openai.com/](https://cdn.gradual.com/images/https://d2xo500swnpgl1.cloudfront.net/uploads/oaiacademy/52-212315c6-2a5f-476d-9c57-071efec17447-1744381706389.png?fit=scale-down&width=345)

![Ads No.1. Click to open https://academy.openai.com/home/clubs/builders-etkn1/resources/gpt-5-for-builders](https://cdn.gradual.com/images/https://d2xo500swnpgl1.cloudfront.net/uploads/oaiacademy/Cover-Image-Ads-Template-for-OAI-Academy-7--f1efdecc-00a6-4ada-86ad-f46bb0f71276-1754593876484.jpeg?fit=scale-down&width=345)

![Ads No.2. Click to open https://academy.openai.com/home/clubs/champions-ecqup/resources/the-ai-champion-role](https://cdn.gradual.com/images/https://d2xo500swnpgl1.cloudfront.net/uploads/oaiacademy/Cover-Image-Ads-Template-for-OAI-Academy-3--d624f8d6-ff05-4a73-9260-3052d65ee598-1754582885148.jpeg?fit=scale-down&width=345)

![Ads No.3. Click to open https://academy.openai.com/home/clubs/admins-6o6xf/resources/empowering-and-supporting-your-team](https://cdn.gradual.com/images/https://d2xo500swnpgl1.cloudfront.net/uploads/oaiacademy/Cover-Image-Ads-Template-for-OAI-Academy-6--a46ca925-14d4-4415-a58b-fc68a4c53a71-1754583943749.jpeg?fit=scale-down&width=345)

![Ads No.4. Click to open https://academy.openai.com/home/clubs/work-users-ynjqu/resources/chatgpt-basics](https://cdn.gradual.com/images/https://d2xo500swnpgl1.cloudfront.net/uploads/oaiacademy/chatgpt-fundamentals-de8f344b-4f84-4f2e-b352-3b995fd68407-1754414334447.jpeg?fit=scale-down&width=345)

![Ads No.5. Click to open https://edunewsletter.openai.com/](https://cdn.gradual.com/images/https://d2xo500swnpgl1.cloudfront.net/uploads/oaiacademy/52-212315c6-2a5f-476d-9c57-071efec17447-1744381706389.png?fit=scale-down&width=345)

![Ads No.1. Click to open https://academy.openai.com/home/clubs/builders-etkn1/resources/gpt-5-for-builders](https://cdn.gradual.com/images/https://d2xo500swnpgl1.cloudfront.net/uploads/oaiacademy/Cover-Image-Ads-Template-for-OAI-Academy-7--f1efdecc-00a6-4ada-86ad-f46bb0f71276-1754593876484.jpeg?fit=scale-down&width=345)

![Ads No.2. Click to open https://academy.openai.com/home/clubs/champions-ecqup/resources/the-ai-champion-role](https://cdn.gradual.com/images/https://d2xo500swnpgl1.cloudfront.net/uploads/oaiacademy/Cover-Image-Ads-Template-for-OAI-Academy-3--d624f8d6-ff05-4a73-9260-3052d65ee598-1754582885148.jpeg?fit=scale-down&width=345)

![Ads No.3. Click to open https://academy.openai.com/home/clubs/admins-6o6xf/resources/empowering-and-supporting-your-team](https://cdn.gradual.com/images/https://d2xo500swnpgl1.cloudfront.net/uploads/oaiacademy/Cover-Image-Ads-Template-for-OAI-Academy-6--a46ca925-14d4-4415-a58b-fc68a4c53a71-1754583943749.jpeg?fit=scale-down&width=345)

![Ads No.4. Click to open https://academy.openai.com/home/clubs/work-users-ynjqu/resources/chatgpt-basics](https://cdn.gradual.com/images/https://d2xo500swnpgl1.cloudfront.net/uploads/oaiacademy/chatgpt-fundamentals-de8f344b-4f84-4f2e-b352-3b995fd68407-1754414334447.jpeg?fit=scale-down&width=345)

![Ads No.5. Click to open https://edunewsletter.openai.com/](https://cdn.gradual.com/images/https://d2xo500swnpgl1.cloudfront.net/uploads/oaiacademy/52-212315c6-2a5f-476d-9c57-071efec17447-1744381706389.png?fit=scale-down&width=345)

## Popular

[Read more about 'ChatGPT and Beyond: How to Handle AI in Schools'](https://academy.openai.com/public/externals/chatgpt-and-beyond-how-to-handle-ai-in-schools-2025-03-11)

External Content

[ChatGPT and Beyond: How to Handle AI in Schools](https://academy.openai.com/public/externals/chatgpt-and-beyond-how-to-handle-ai-in-schools-2025-03-11)

[1:01:15](https://academy.openai.com/public/clubs/k-12-education-aacga/videos/intro-to-ai-for-k-12-educators-2025-04-01)

Video

[Intro to AI for K-12 Educators](https://academy.openai.com/public/clubs/k-12-education-aacga/videos/intro-to-ai-for-k-12-educators-2025-04-01)

BySam Canning-Kaplan

[44:20](https://academy.openai.com/public/clubs/work-users-ynjqu/videos/chatgpt-101-a-guide-to-your-ai-superassistant-recording)

Video

[ChatGPT 101: A Guide to Your AI Superassistant \[Recording\]](https://academy.openai.com/public/clubs/work-users-ynjqu/videos/chatgpt-101-a-guide-to-your-ai-superassistant-recording)

Dive in

## Related

[Read more about 'How Alex Lupsasca learned to trust AI for real physics'](https://academy.openai.com/public/blogs/alex-lupsasca-gpt-5-pro-black-hole-physics-hidden-symmetries)

Blog

[How Alex Lupsasca learned to trust AI for real physics](https://academy.openai.com/public/blogs/alex-lupsasca-gpt-5-pro-black-hole-physics-hidden-symmetries)

Feb 2nd, 2026 • Views 1.7K

[25:00](https://academy.openai.com/public/videos/using-workspace-analytics-to-drive-adoption-2026-04-08)

Video

[Using workspace analytics to drive adoption](https://academy.openai.com/public/videos/using-workspace-analytics-to-drive-adoption-2026-04-08)

Apr 8th, 2026 • Views 1.2K

[Read more about 'Terence Tao: AI is ready for primetime in math and theoretical physics'](https://academy.openai.com/public/blogs/terence-tao-ai-is-ready-for-primetime-in-math-and-theoretical-physics-2026-03-06)

Blog

[Terence Tao: AI is ready for primetime in math and theoretical physics](https://academy.openai.com/public/blogs/terence-tao-ai-is-ready-for-primetime-in-math-and-theoretical-physics-2026-03-06)

Mar 6th, 2026 • Views 3.4K

[10:39](https://academy.openai.com/public/videos/using-chatgpt-to-spot-scams-2025-09-25)

Video

[Using ChatGPT to Spot Scams](https://academy.openai.com/public/videos/using-chatgpt-to-spot-scams-2025-09-25)

By Jack Stubbs • Sep 26th, 2025 • Views 8.9K

[Read more about 'How Alex Lupsasca learned to trust AI for real physics'](https://academy.openai.com/public/blogs/alex-lupsasca-gpt-5-pro-black-hole-physics-hidden-symmetries)

Blog

[How Alex Lupsasca learned to trust AI for real physics](https://academy.openai.com/public/blogs/alex-lupsasca-gpt-5-pro-black-hole-physics-hidden-symmetries)

Feb 2nd, 2026 • Views 1.7K

[Read more about 'Terence Tao: AI is ready for primetime in math and theoretical physics'](https://academy.openai.com/public/blogs/terence-tao-ai-is-ready-for-primetime-in-math-and-theoretical-physics-2026-03-06)

Blog

[Terence Tao: AI is ready for primetime in math and theoretical physics](https://academy.openai.com/public/blogs/terence-tao-ai-is-ready-for-primetime-in-math-and-theoretical-physics-2026-03-06)

Mar 6th, 2026 • Views 3.4K

[10:39](https://academy.openai.com/public/videos/using-chatgpt-to-spot-scams-2025-09-25)

Video

[Using ChatGPT to Spot Scams](https://academy.openai.com/public/videos/using-chatgpt-to-spot-scams-2025-09-25)

By Jack Stubbs • Sep 26th, 2025 • Views 8.9K

[25:00](https://academy.openai.com/public/videos/using-workspace-analytics-to-drive-adoption-2026-04-08)

Video

[Using workspace analytics to drive adoption](https://academy.openai.com/public/videos/using-workspace-analytics-to-drive-adoption-2026-04-08)

Apr 8th, 2026 • Views 1.2K

We use cookies to keep the platform secure and improve your experience. Essential cookies are always active. You can manage optional cookies anytime. [Cookie Policy](https://gradual.notion.site/Gradual-Cookie-Policy-3586c5d5c70c80a89d0fdc74072d276c)

Accept AllReject AllManage Preferences

Twitter Widget Iframe