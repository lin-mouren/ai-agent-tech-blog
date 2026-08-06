---
title: "Securing Android AI interoperability in Europe"
vendor: google
source_url: https://blog.google/security/android-ai-security-eu-dma/
published_at: 2026-08-05T01:00:00.000Z
crawled_at: 2026-08-06T02:00:39.431Z
word_count: 2681
reading_time_minutes: 14
tags: [gpt, safety, agents, api, product, enterprise, open-source]
---

[Android](https://blog.google/products-and-platforms/platforms/android/)

# Balancing Interoperability and Security in the Age of AI

Aug 05, 2026

\|

9 min read

- [x.com](https://twitter.com/intent/tweet?text=Balancing%20Interoperability%20and%20Security%20in%20the%20Age%20of%20AI%20%40google&url=https://blog.google/security/android-ai-security-eu-dma/)
- [Facebook](https://www.facebook.com/sharer/sharer.php?caption=Balancing%20Interoperability%20and%20Security%20in%20the%20Age%20of%20AI&u=https://blog.google/security/android-ai-security-eu-dma/)
- [LinkedIn](https://www.linkedin.com/shareArticle?mini=true&url=https://blog.google/security/android-ai-security-eu-dma/&title=Balancing%20Interoperability%20and%20Security%20in%20the%20Age%20of%20AI)
- [Mail](mailto:?subject=Balancing%20Interoperability%20and%20Security%20in%20the%20Age%20of%20AI&body=Check%20out%20this%20article%20on%20the%20Keyword:%0A%0ABalancing%20Interoperability%20and%20Security%20in%20the%20Age%20of%20AI%0A%0Ahttps://blog.google/security/android-ai-security-eu-dma/)
- Copy link


* * *

Dave Kleidermacher

VP Engineering, Android Security & Privacy

Eugene Liderman

Director, Android Security & Privacy

Share


- [x.com](https://twitter.com/intent/tweet?text=Balancing%20Interoperability%20and%20Security%20in%20the%20Age%20of%20AI%20%40google&url=https://blog.google/security/android-ai-security-eu-dma/)
- [Facebook](https://www.facebook.com/sharer/sharer.php?caption=Balancing%20Interoperability%20and%20Security%20in%20the%20Age%20of%20AI&u=https://blog.google/security/android-ai-security-eu-dma/)
- [LinkedIn](https://www.linkedin.com/shareArticle?mini=true&url=https://blog.google/security/android-ai-security-eu-dma/&title=Balancing%20Interoperability%20and%20Security%20in%20the%20Age%20of%20AI)
- [Mail](mailto:?subject=Balancing%20Interoperability%20and%20Security%20in%20the%20Age%20of%20AI&body=Check%20out%20this%20article%20on%20the%20Keyword:%0A%0ABalancing%20Interoperability%20and%20Security%20in%20the%20Age%20of%20AI%0A%0Ahttps://blog.google/security/android-ai-security-eu-dma/)
- Copy link


* * *

Over the last six months, we have been engaging closely with the European Commission (EC) after they opened [specification proceedings](https://ec.europa.eu/commission/presscorner/detail/en/ip_26_202) related to Android interoperability for AI services, pursuant to the EU Digital Markets Act (DMA). At the center of this engagement is the EC’s desire to mandate that Android provides user-downloaded artificial intelligence (AI) agents with deep system-level access to powerful device capabilities. While the EC’s interoperability objectives align with Android's history and mission as an open ecosystem, the [final measures](https://ec.europa.eu/competition/digital_markets_act/cases/202629/DMA_100220_2683.pdf) undermine Android’s foundational security model, placing European consumers’ privacy, security, and safety at risk.

As the specification proceedings enter the implementation phase, we urge the EC to properly account for these risks through consultations with cybersecurity experts (many of whom have co-signed this blogpost) and ensure that necessary safeguards remain in place to protect Android users in Europe.

## **Where we started**

The Android ecosystem already fosters a vibrant, competitive AI market. Today, prominent user-downloadable AI services like ChatGPT, Claude, and Perplexity are used by tens of millions of consumers daily on Android, operating securely within their app sandboxes and supported by Android’s robust developer tools. Meanwhile, Android device manufacturers bring even more deeply integrated experiences to their devices, both through their own innovative features and by partnering with third-party AI developers that they have vetted \[ [1](https://www.samsung.com/us/support/answer/ANS10010357/), [2](https://en-us.support.motorola.com/app/answers/detail/a_id/185053/~/moto-ai-%7C-ask-or-search-with-moto-ai)\].

Consumers expect Google and Android device manufacturers, as the stewards of the Android ecosystem, to ensure the security and privacy of their devices, especially for apps that are deeply embedded and granted access to highly sensitive capabilities, such as those at issue in these EC proceedings. Third parties simply do not have the same incentives to protect the safety of consumers’ devices. Android, through its open-source architecture and this model of vetted partnerships between device manufacturers and app developers, has already struck a balance between innovation and competition, on the one hand, and the safety and security of the ecosystem, on the other.

## **Where we are heading**

Throughout the proceedings our senior engineers and security experts spent significant time with the EC in technical meetings, exploring how we could potentially open up Android even further while ensuring it remains a secure ecosystem.

Despite these efforts, the EC’s specifications mandate a fundamental overhaul of Android's security architecture, overlooking that this proven security model has already created the world's most open and interoperable mobile operating system for AI innovation. It is not surprising that when the EC published its draft measures in April, independent security experts sounded the alarm:

- " _I can state with both knowledge and certainty that the European Commission’s technical proposals (or draft measures) are dangerous for the security of every citizen of this world, and they represent gross overreach._" David Rogers MBE, CEO at Copper Horse and Former GSMA Fraud & Security Group Chair ( [link](https://mobilephonesecurity.org/2026/07/when-good-intentions-facilitate-the-really-bad-guys/))
- " _Opening capabilities first and adding protection later is how this risk becomes incidents; establishing the limits in advance is how interoperability and security come to reinforce one another rather than work against each other._" Rubén Lirio, Global Cybersecurity Director at DEKRA, a EU Cybersecurity Lab and [Notified Body](https://single-market-economy.ec.europa.eu/single-market/goods/building-blocks/notified-bodies_en) ( [link](https://www.dekra.com/en/ai-agents-for-security-and-eu-regulations/))

While we are encouraged by positive progress since the Preliminary Findings, we continue to have very significant concerns that the final measures introduce several security loopholes, leaving European users vulnerable to mobile threats in the age of AI.

The table at the bottom of this post outlines just some of the risks the proposed measures would introduce, as well as potential conflicts with existing EU cybersecurity regulations and standards

[1](https://blog.google/security/android-ai-security-eu-dma/#footnote-1)
. As we move forward with the EC on implementation, it is crucial that these issues receive full consideration through direct consultation with cybersecurity experts and ecosystem stakeholders.

## **Modern fraud capitalizes on AI**

The EC’s final measures underestimate the grim reality of modern fraud. As consumers increasingly rely on mobile devices for banking, private communications, and managing their digital identities, phones have become the primary target for malicious actors. Scammers are increasingly leveraging generative AI to deploy highly sophisticated social engineering scripts, hyper-realistic deepfakes, and polymorphic malware:

- **Annual global scam losses have climbed to roughly 1% of global GDP**. According to the Global Anti-Scam Alliance, **$442 billion** was lost to scams in one year and over **73%** of the respondents experienced an online scam or attack in the last year.


[2](https://blog.google/security/android-ai-security-eu-dma/#footnote-2)
- **The vast majority of scams now begin on mobile devices**. According to Pew Research Center, **68%** receive a scam call weekly and **61%** receive a scam text weekly.


[3](https://blog.google/security/android-ai-security-eu-dma/#footnote-3)
- **Users are facing daily threats of mobile scams**. A 2025 report by Malwarebytes found that **44%** of surveyed global users encounter a mobile scam every single day. This report also found that of the **36%** of users who have fallen victim to a mobile scam, **52%** suffered direct financial loss or fraud, and **27%** lost access to critical digital assets or accounts.


[4](https://blog.google/security/android-ai-security-eu-dma/#footnote-4)
- **Scammers are weaponizing generative AI**. Over **80%** of phishing emails are AI generated, deepfake fraud attempts have risen by **2,000%** since 2022, and around **3 in 4** AI voice scam victims have lost money as a result.


[5](https://blog.google/security/android-ai-security-eu-dma/#footnote-5)
- **AI-powered fraud has surged to an industrial scale**. AI scams growing by over **1,210%**. The FBI recorded over **22,000** AI-related complaints in a single year, costing people nearly $893 million. Experts project that U.S. losses alone from generative AI fraud will hit **$40 billion** by 2027.


[6](https://blog.google/security/android-ai-security-eu-dma/#footnote-6)

We appreciate that the EC’s final measures allow a qualification process for a subset of the features at issue. However, this safeguard is only effective if we are allowed to implement it robustly. A qualification process without strong platform enforcement is mere security theater. Furthermore, it is alarming that a number of other sensitive features – including access to ambient data such as always-on microphone, camera, and on-screen content – are denied this protection and must be made available to any app. This significant exception ignores a dangerous reality: giving any unvetted app continuous, hidden background access to microphones and screens is precisely the capability that malware authors covet and exploit.

In addition, even where the final measures allow for a qualification process, the EC mandates that users be given a mechanism to bypass these protections entirely, granting high-risk capabilities like screen automation to any app. As we emphasized to the EC throughout the proceedings, these kinds of loopholes are a gift to scammers who regularly use social engineering to trick vulnerable users into handing over access to their most sensitive data.

Experts agree on the dangers of creating such loopholes in the name of interoperability. As Ashwini Rao, Co-Founder and CEO of Eydle, points out: " _To balance innovation with user safety, mandates must incorporate a risk-based approach to interoperability. We must consider the risk from distinct vectors (Access Level, Data Scope, Action Type) and Consent Fatigue, which is exponentially worse due to continuous multi-step tasks. Otherwise, we are pushing the security and approval burden onto the users and leaving them vulnerable._"

The EC’s final measures risk dismantling the multi-layered defense-in-depth strategy Android employs to keep users safe. As [Forrester](https://www.forrester.com/), a major business and technology research company, noted in their [recent blog post](https://www.forrester.com/blogs/the-eus-digital-markets-act-meets-the-mobile-os-round-2-can-the-push-for-a-fair-fight-go-too-far/): “ _the EU Commissioners are playing with fire._” Mitigating this risk needs to be a top priority for all stakeholders in the implementation phase.

## **Nascent technologies introduce novel risks and threats**

AI agents are a rapidly developing and highly dynamic technology, which significantly heightens risks to users. Without sufficient safeguards, an insecure agent can become the primary attack vector through exploits like indirect prompt injection, where hidden instructions in external data hijack the agent’s behavior. When an autonomous agent is granted deep, low-level system access without vetting by the operating system or device manufacturer, the real world consequences are severe. This is not a hypothetical threat; it has been widely documented by security researchers, reported in the media, and echoed across the industry:

- [Apple](https://www.apple.com/newsroom/2026/06/due-to-dma-siri-ai-delayed-in-eu-for-ios-27-and-ipados-27/): “ _Security researchers have already shown that AI systems can be hijacked to steal personal data — like passwords and photos — and to permanently alter files and account settings without a user’s consent. As AI systems gain more capabilities, these risks are quickly increasing in frequency and scope.”_
- [Eydle](https://www.eydle.com/): " _Granting deep system access to third-party AI-related services introduces a paradigm shift in threat modeling. Traditional applications are deterministic, but AI agents are not. Ensuring integrity requires new frameworks to measure and verify the safety of non-deterministic AI systems, and these frameworks are still evolving. Mandates must consider this to ensure that we balance pace of innovation with user safety.”_

Even other branches of the European Commission recognize these evolving threats. Just this week, as the EC began enforcing the EU AI Act, its own AI Office [highlighted](https://www.reuters.com/world/eu-says-necessary-monitor-high-risk-ai-systems-after-openai-anthropic-ai-hacking-2026-07-31/) the need to evaluate the unique safety and security risks of agentic use, acknowledging that regulatory strategies for AI agents are still in preliminary stages.

Given these novel risks, standards development organizations and industry associations are still in the early stages of defining appropriate security and privacy guardrails. The European Telecommunications Standards Institute (ETSI) only released their standard for Securing Artificial Intelligence (SAI); Baseline Cyber Security Requirements for AI Models and Systems in December 2025, a high level standard that does not yet address the nuances of agentic threats. In similar regulatory contexts, it has been important to ensure that cybersecurity experts have sufficient time to map risks to technical standards, compliance tools, and platform controls. For example, in a [blog post](https://www.brightsight.com/news/post/building-trust-in-europe-s-digital-market-the-role-of-assurance-in-a-changing-regulatory-landscape), Sergio Casanova, CTO at Brightsight noted that _“recent changes to the EU AI Act timeline have underscored the value of preparation. The additional time before full implementation gives organizations an opportunity to understand the requirements more clearly, improve internal processes, and strengthen their approach to risk and assurance._"

While the EC’s final measures allow for a qualification process, they also mandate the creation of a Trusted Certification Authorities (TCAs) program that would allow apps to complete the process and gain access to restricted features through a third-party, without any oversight by Google or device manufacturers. We welcome the potential to leverage independent third-party expertise to inform our evaluations. However, given the novel risks and early stages in developing an effective security model, Google and device manufacturers—the entities with the comprehensive threat intelligence, system-level telemetry, and direct accountability to protect users—must retain the authority for maintaining the certification lifecycle for agents, including approval, suspension, and revocation, to ensure these measures do not compromise ecosystem safety. By integrating third-party assessments into a process where Google maintains final review and enforcement, we can strike the right balance, keeping European consumers safe while supporting an interoperable ecosystem.

## **The importance of security by design: EU cybersecurity regulation**

It is striking that these final measures come at a time when the EU is reinforcing the foundational principles of "security-by-design" and "security-by-default" across its broader cybersecurity regulations. Enforcing competition rules in isolation creates a direct tension with cybersecurity policy, one that must be carefully managed to avoid putting users at risk.

Testing and certification lab DEKRA highlighted this exact friction in their June [blog post](https://www.dekra.com/en/ai-agents-for-security-and-eu-regulations/): “ _This is where the two regulations come into direct conflict in the context of AI agents for security. The DMA seeks to open these powerful capabilities to third-party agents, whereas the CRA seeks to keep the device's exposure to a minimum._"

Industry experts emphasize that these two priorities must work in tandem. As Jose Ruiz, Cybersecurity BU Director at Applus+ Laboratories, noted: “ _Applus+ Laboratories welcomes initiatives that promote innovation, interoperability, and consumer choice across the digital ecosystem. At the same time, any evolution of platform access models should be carefully assessed to ensure continued compliance with security-by-design principles and the objectives of the Cyber Resilience Act. Achieving both competition and cybersecurity is not only possible, but essential for maintaining user trust and the long-term resilience of digital services._”

## **Looking forward**

As we enter the implementation phase, we want to be clear: implementing these measures without rigorous security safeguards risks irreparable harm to device manufacturers, app developers, and most importantly, consumers.

As an open platform that has long championed interoperability, Android has consistently demonstrated that interoperability and security can coexist. To maintain this balance, platforms must retain the authority to enforce rigorous guardrails while working alongside cybersecurity experts to define baseline criteria. This collaborative approach ensures AI agents can innovate safely without opening backdoors for malicious actors to exploit.

It is critically important that the application of the final measures during the implementation phase reflects a shared commitment to balancing interoperability and security in the age of AI.

Below are some of the independent experts who support our call to deeply consult cybersecurity professionals, ensuring European consumers are not left with weaker protections than the rest of the world.

Signed by:

01. Rubén Lirio, Global Cybersecurity Director at [DEKRA](https://www.dekra.com/en/cybersecurity-services/)
02. Jose Ruiz, Cybersecurity BU Director at [Applus+ Laboratories](https://www.appluslaboratories.com/global/en/)
03. Sergio Casanova, Chief Technology Officer at [SGS](https://www.sgs.com/en/industry/cybersecurity-and-technology/cybersecurity-services)
04. Thai Duong, Chief at [Calif](https://calif.io/)
05. David Rogers MBE, CEO at [Copper Horse](https://copperhorse.co.uk/)
06. Amit Elazari, CEO and Co-Founder of [OpenPolicy](https://www.openpolicy.co/)
07. Tatyana Bolton, Head of Cyber Practice at [Monument Advocacy](https://monumentadvocacy.com/)
08. Alan Snyder, CEO at [NowSecure](https://www.nowsecure.com/)
09. Frank Heidt, Managing Director at [Leviathan Security Group](https://www.leviathansecurity.com/)
10. Ashwini Rao, Co-Founder and CEO at [Eydle](https://www.eydle.com/)
11. Joel Scambray, Senior Vice President of Technical Assurance Services at [NCC Group](https://www.nccgroup.com/)
12. Wouter Slegers, CEO at [TrustCB](https://www.trustcb.com/) (EUCC & SESIP Certification Body and Notified Body for eIDAS and CRA)

[](https://services.google.com/fh/files/misc/technicalanalysis_keywordblog_2352x1458.png)

POSTED IN:

Read more

* * *

More Information

* * *

[1](https://blog.google/security/android-ai-security-eu-dma/#footnote-source-1 "Jump up")

Quick summary of the relevant cybersecurity regulations and their respective standards:

**EU Radio Equipment Directive (RED) Delegated Act** and its harmonized standard (EN 18031) which covers network protection (3.3d), privacy and data protection (3.3e), and fraud prevention (3.3f).

**EU Cyber Resilience Act** which mandates products with digital elements follow strict "security-by-design and security-by-default protocols (Annex I). It requires manufacturers to exercise due diligence to ensure third-party components do not compromise product security. The draft vertical standard for operating systems (ETSI EN 304 626) outlines essential cybersecurity requirements for operating systems, defining technical controls for things like access control, memory isolation, and availability. ETSI also defined a Consumer Mobile Device Protection Profile which is the only EU-based smartphone security standard focusing on things like asset isolation, biometric security, and bootloader integrity.

[2](https://blog.google/security/android-ai-security-eu-dma/#footnote-source-2 "Jump up")

[https://gasa.org/knowledge-base/reports/global-state-of-scams-2025](https://gasa.org/knowledge-base/reports/global-state-of-scams-2025)

[3](https://blog.google/security/android-ai-security-eu-dma/#footnote-source-3 "Jump up")

[https://www.pewresearch.org/internet/2025/07/31/online-scams-and-attacks-in-america-today/](https://www.pewresearch.org/internet/2025/07/31/online-scams-and-attacks-in-america-today/)

[4](https://blog.google/security/android-ai-security-eu-dma/#footnote-source-4 "Jump up")

[https://www.malwarebytes.com/blog/scams/2025/06/44-of-people-encounter-a-mobile-scam-every-single-day-malwarebytes-finds](https://www.malwarebytes.com/blog/scams/2025/06/44-of-people-encounter-a-mobile-scam-every-single-day-malwarebytes-finds)

[5](https://blog.google/security/android-ai-security-eu-dma/#footnote-source-5 "Jump up")

[https://programs.com/resources/ai-cyberattack-stats/](https://programs.com/resources/ai-cyberattack-stats/)

[6](https://blog.google/security/android-ai-security-eu-dma/#footnote-source-6 "Jump up")

[https://www.fbi.gov/news/press-releases/cryptocurrency-and-ai-scams-bilk-americans-of-billions](https://www.fbi.gov/news/press-releases/cryptocurrency-and-ai-scams-bilk-americans-of-billions)

Collapse

* * *

## Latest stories

[Security\\
**Influence Operations Bulletin Q2 2026** \\
\\
This bulletin includes coordinated influence operation campaigns terminated on our platforms in Q2 2026. It was last updated on June 30, 2026.AprilWe terminated 13 YouTu…\\
\\
By\\
\\
\\
Trust & Safety](https://blog.google/security/influence-operations-bulletin-q2-2026/)

[\\
\\
Chrome\\
**Stronger with every update: How we’re making Chrome and the web safer in the AI Era**\\
\\
By\\
\\
\\
Chrome Security Team](https://blog.google/security/chrome-stronger-with-every-update/)

[Security\\
**From Finding to Fixing: Reducing maintainer burden with automated patches** \\
\\
Since its launch in 2016, OSS-Fuzz has contributed significantly to making open-source secure by finding and reporting tens of thousands of bugs. But finding more vulner…\\
\\
By\\
\\
\\
Alex Kilian\\
\\
& \\
Dustin Ingram](https://blog.google/security/from-finding-to-fixing-reducing-maintainer-burden-with-automated-patches/)

[\\
\\
Security\\
**Going Beyond Zero: A New Paradigm For Enterprise Security**\\
\\
By\\
\\
\\
Heather Adkins\\
\\
& \\
Archana Ramamoorthy](https://blog.google/security/going-beyond-zero-a-new-paradigm-for-enterprise-security/)

[\\
\\
Android Security\\
**How Android helps keep you safe from impersonation scams with fake call detection**\\
\\
By\\
\\
\\
Eric Lynch\\
\\
& \\
Troy Kensinger\\
\\
& \\
Oren Schetrit](https://blog.google/security/android-fake-call-detection/)

[\\
\\
Chrome Security\\
**Bringing AI agents to Chrome Enterprise security management**\\
\\
By\\
\\
\\
Tim Feeley\\
\\
& \\
Shantanu Das](https://blog.google/security/bringing-ai-agents-to-chrome-enterprise-security-management/)