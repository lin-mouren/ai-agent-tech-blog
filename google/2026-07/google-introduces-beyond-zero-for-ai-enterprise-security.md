---
title: "Google introduces Beyond Zero for AI enterprise security"
vendor: google
source_url: https://blog.google/security/going-beyond-zero-a-new-paradigm-for-enterprise-security/
published_at: 2026-07-27T16:00:00.000Z
crawled_at: 2026-07-28T02:00:45.074Z
word_count: 1170
reading_time_minutes: 6
tags: [gemini, multimodal, safety, agents, product, enterprise]
---

[Security](https://blog.google/security/)

# Going Beyond Zero: A New Paradigm For Enterprise Security

Jul 27, 2026

\|

3 min read

- [x.com](https://twitter.com/intent/tweet?text=Going%20Beyond%20Zero%3A%20A%20New%20Paradigm%20For%20Enterprise%20Security%20%40google&url=https://blog.google/security/going-beyond-zero-a-new-paradigm-for-enterprise-security/)
- [Facebook](https://www.facebook.com/sharer/sharer.php?caption=Going%20Beyond%20Zero%3A%20A%20New%20Paradigm%20For%20Enterprise%20Security&u=https://blog.google/security/going-beyond-zero-a-new-paradigm-for-enterprise-security/)
- [LinkedIn](https://www.linkedin.com/shareArticle?mini=true&url=https://blog.google/security/going-beyond-zero-a-new-paradigm-for-enterprise-security/&title=Going%20Beyond%20Zero%3A%20A%20New%20Paradigm%20For%20Enterprise%20Security)
- [Mail](mailto:?subject=Going%20Beyond%20Zero%3A%20A%20New%20Paradigm%20For%20Enterprise%20Security&body=Check%20out%20this%20article%20on%20the%20Keyword:%0A%0AGoing%20Beyond%20Zero%3A%20A%20New%20Paradigm%20For%20Enterprise%20Security%0A%0ALearn%20about%20Beyond%20Zero,%20Google%27s%20new%20risk-based%20enterprise%20security%20paradigm%20designed%20for%20the%20AI%20era.%0A%0Ahttps://blog.google/security/going-beyond-zero-a-new-paradigm-for-enterprise-security/)
- Copy link


* * *

[Heather Adkins\\
\\
VP, Security Engineering](https://blog.google/authors/heather-adkins/)

Archana Ramamoorthy

Senior Director, Cybersecurity and Data Protection

Share


- [x.com](https://twitter.com/intent/tweet?text=Going%20Beyond%20Zero%3A%20A%20New%20Paradigm%20For%20Enterprise%20Security%20%40google&url=https://blog.google/security/going-beyond-zero-a-new-paradigm-for-enterprise-security/)
- [Facebook](https://www.facebook.com/sharer/sharer.php?caption=Going%20Beyond%20Zero%3A%20A%20New%20Paradigm%20For%20Enterprise%20Security&u=https://blog.google/security/going-beyond-zero-a-new-paradigm-for-enterprise-security/)
- [LinkedIn](https://www.linkedin.com/shareArticle?mini=true&url=https://blog.google/security/going-beyond-zero-a-new-paradigm-for-enterprise-security/&title=Going%20Beyond%20Zero%3A%20A%20New%20Paradigm%20For%20Enterprise%20Security)
- [Mail](mailto:?subject=Going%20Beyond%20Zero%3A%20A%20New%20Paradigm%20For%20Enterprise%20Security&body=Check%20out%20this%20article%20on%20the%20Keyword:%0A%0AGoing%20Beyond%20Zero%3A%20A%20New%20Paradigm%20For%20Enterprise%20Security%0A%0ALearn%20about%20Beyond%20Zero,%20Google%27s%20new%20risk-based%20enterprise%20security%20paradigm%20designed%20for%20the%20AI%20era.%0A%0Ahttps://blog.google/security/going-beyond-zero-a-new-paradigm-for-enterprise-security/)
- Copy link


* * *



At Google, we’ve spent decades trying to push the limits of what is possible in security. In 2014, we released the [BeyondCorp whitepaper](https://www.usenix.org/system/files/login/articles/login_dec14_02_ward.pdf), describing the beginnings of what became a near decade-long push to establish zero trust as the desired model for securing enterprise networks. We’re pleased to reflect on the success of our internal adoption of BeyondCorp and see the benefits that it has brought to our users in keeping them safer. It has also enabled our company as a whole to transition to a more secure way of working without compromising our own agility and ability to innovate. Likewise, it has been wonderful to see the success of other enterprises and the security industry more broadly in adopting zero trust as the standard for what good enterprise security looks like. Security is ultimately a collaborative endeavor, and when good ideas and design patterns are shared with the broader industry we only stand to gain from the many learnings that come back to us.

The enterprise landscape is now entering a new era shaped by artificial intelligence, where AI is changing the assumptions around how enterprise security works. AI agents are being deployed globally to increase operational velocity and boost productivity. However, this increased capability also presents new potential risks, as attackers can leverage similar speed to compromise privileged credentials and execute attacks. This creates the need for a new security paradigm that is capable of defending against these new threats.

## **Introducing Beyond Zero**

**Beyond Zero** is a new security paradigm designed to address these AI-era challenges with a contextual, risk-based, resource-level authorization model to run at machine-speed, securing both humans and agents without overburdening the user experience. This extends the concepts from zero trust into the authorization layer, ensuring that every single action taken inside an enterprise is authorized.

The **Beyond Zero** model is built on five core principles:

1. **Resource and Action-based security**: Authorization decisions are evaluated at the level of individual actions on specific resources, rather than granting broad access to an entire application or tool. This applies uniformly across all access methods, including front-end interfaces, APIs, and the Model Context Protocol (MCP).
2. **Blended static and dynamic security:** Granular static policies are paired with dynamic controls that apply heightened security measures during high-risk or complex scenarios. This approach introduces dynamic protections without moving to a fully dynamic model, which can be difficult to verify statically.
3. **Automatically enriched context:** The decision systems can draw on context about the user action, what the user should be working on, what data the user action is trying to interact with, what the user action is attempting to do with the data, and what potential risk mitigations are available. These facts are always available to the decision making infrastructure.
4. **Automated in-depth investigation:** Risk signals can autonomously trigger security investigations, which can immediately deploy user challenges or containment measures across the access stream.
5. **Challenges and containments:** Security policies can directly trigger verification challenges or containment protocols, requiring users or agents to provide additional risk telemetry on demand.

Early internal prototypes and deployments of Beyond Zero are showing improved access abuse detection, intellectual property protection, as well as allowing us to run our business at pace while abiding by the many regulatory and other specialized control offerings needed by our customers. We will continue to share additional technical details and deployment strategies as our work progresses.

## **Sharing Beyond Zero with the Industry**

Google is introducing Beyond Zero to the broader security community through a series of technical publications. The first paper, [_Beyond Zero: Enterprise Security for the AI Era_](https://spawn-queue.acm.org/doi/10.1145/3819083), has been published in ACM Queue. This initial paper outlines the foundational vision for Beyond Zero and details the architecture developed within Alphabet.

Subsequent papers will be released over time to share ongoing implementation data and operational insights, following a publication model similar to the original BeyondCorp series.

While industry-wide adoption of continuous authorization is in its early stages, peer organizations and industry bodies are beginning to develop comparable frameworks that are described in _Beyond Zero_. Google remains committed to collaborating with industry partners to refine these techniques and advance collective enterprise security standards.

_Beyond Zero_ connects with other research being done inside Alphabet, intersecting with enterprise security questions in both the AI and non-AI domains. Our recent [DeepMind Security publication](https://deepmind.google/blog/securing-the-future-of-ai-agents/) on AI Agent Security shows the importance of real-time access controls and automated monitoring when deploying agents within sensitive corporate environments. Broader work in the industry on human-centered zero-trust paradigms have also reiterated the need to continue pushing the boundary of security to smaller scopes of trust.

## **Pushing Google and the Industry Beyond Zero**

This is the first of several forthcoming publications on Beyond Zero. As we did with prior security publications, we will provide details on our progress, the architectural and operational / implementation considerations that went into this achievement, as well as ideas for how the industry can come together to help advance the state of technology so that everyone can benefit. We thank everyone from the industry whose ideas have contributed to our work and we look forward to sharing more soon.

POSTED IN:

## Related stories

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

[Security\\
**Influence Operations Bulletin Q1 2026** \\
\\
This bulletin includes coordinated influence operation campaigns terminated on our platforms in Q1 2026. It was last updated on March 31, 2026.JanuaryWe terminated 40 Yo…\\
\\
By\\
\\
\\
Trust & Safety](https://blog.google/security/influence-operations-bulletin-q1-2026/)

[Security\\
**AI threats in the wild: The current state of prompt injections on the web** \\
\\
We initiated a broad sweep of the public web to monitor for known indirect prompt injection patterns. This is what we found.\\
\\
By\\
\\
\\
Thomas Brunner\\
\\
& \\
Yu-Han Liu\\
\\
& \\
Moni Pande](https://blog.google/security/prompt-injections-web/)

[Security\\
**Protecting Cookies with Device Bound Session Credentials** \\
\\
Following our April 2024 announcement, Device Bound Session Credentials (DBSC) is now entering public availability for Windows users on Chrome 146, and expanding to macO…\\
\\
By\\
\\
\\
Benjamin Ackerman\\
\\
& \\
Daniel Rubery\\
\\
& \\
Guillaume Ehinger](https://blog.google/security/protecting-cookies-with-device-bound-session-credentials/)

[Security\\
**Google Workspace’s continuous approach to mitigating indirect prompt injections** \\
\\
Indirect prompt injection (IPI) is an evolving threat vector targeting users of complex AI applications with multiple data sources, such as Workspace with Gemini. This t…\\
\\
By\\
\\
\\
Adam Gavish\\
\\
& \\
Google GenAI Security Team](https://blog.google/security/google-workspaces-continuous-approach-to-mitigating-indirect-prompt-injections/)

[\\
\\
Security\\
**Staying One Step Ahead: Strengthening Android’s Lead in Scam Protection**\\
\\
By\\
\\
\\
Lyubov Farafonova\\
\\
& \\
Alberto Pastor Nieto](https://blog.google/security/strengthening-android-lead-in-scam-protection/)