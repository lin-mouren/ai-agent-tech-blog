---
title: "How Google is Making Private AI Practical with Homomorphic Encryption"
vendor: google
source_url: https://blog.google/security/how-google-is-making-private-ai-practical-with-homomorphic-encryption/
published_at: 2026-08-14T14:00:00.000Z
crawled_at: 2026-08-15T02:00:59.500Z
word_count: 977
reading_time_minutes: 5
tags: [gpt, multimodal, safety, agents, infrastructure, evaluation, api, research, product, enterprise]
---

[Security](https://blog.google/security/)

# How Google is Making Private AI Practical with Homomorphic Encryption

Aug 14, 2026

\|

3 min read

- [x.com](https://twitter.com/intent/tweet?text=How%20Google%20is%20Making%20Private%20AI%20Practical%20with%20Homomorphic%20Encryption%20%40google&url=https://blog.google/security/how-google-is-making-private-ai-practical-with-homomorphic-encryption/)
- [Facebook](https://www.facebook.com/sharer/sharer.php?caption=How%20Google%20is%20Making%20Private%20AI%20Practical%20with%20Homomorphic%20Encryption&u=https://blog.google/security/how-google-is-making-private-ai-practical-with-homomorphic-encryption/)
- [LinkedIn](https://www.linkedin.com/shareArticle?mini=true&url=https://blog.google/security/how-google-is-making-private-ai-practical-with-homomorphic-encryption/&title=How%20Google%20is%20Making%20Private%20AI%20Practical%20with%20Homomorphic%20Encryption)
- [Mail](mailto:?subject=How%20Google%20is%20Making%20Private%20AI%20Practical%20with%20Homomorphic%20Encryption&body=Check%20out%20this%20article%20on%20the%20Keyword:%0A%0AHow%20Google%20is%20Making%20Private%20AI%20Practical%20with%20Homomorphic%20Encryption%0A%0Ahttps://blog.google/security/how-google-is-making-private-ai-practical-with-homomorphic-encryption/)
- Copy link


* * *

Jeremy Kun

Staff Software Engineer

Share


- [x.com](https://twitter.com/intent/tweet?text=How%20Google%20is%20Making%20Private%20AI%20Practical%20with%20Homomorphic%20Encryption%20%40google&url=https://blog.google/security/how-google-is-making-private-ai-practical-with-homomorphic-encryption/)
- [Facebook](https://www.facebook.com/sharer/sharer.php?caption=How%20Google%20is%20Making%20Private%20AI%20Practical%20with%20Homomorphic%20Encryption&u=https://blog.google/security/how-google-is-making-private-ai-practical-with-homomorphic-encryption/)
- [LinkedIn](https://www.linkedin.com/shareArticle?mini=true&url=https://blog.google/security/how-google-is-making-private-ai-practical-with-homomorphic-encryption/&title=How%20Google%20is%20Making%20Private%20AI%20Practical%20with%20Homomorphic%20Encryption)
- [Mail](mailto:?subject=How%20Google%20is%20Making%20Private%20AI%20Practical%20with%20Homomorphic%20Encryption&body=Check%20out%20this%20article%20on%20the%20Keyword:%0A%0AHow%20Google%20is%20Making%20Private%20AI%20Practical%20with%20Homomorphic%20Encryption%0A%0Ahttps://blog.google/security/how-google-is-making-private-ai-practical-with-homomorphic-encryption/)
- Copy link


* * *

Today we're excited to showcase [HEIR](https://heir.dev/), the latest powerful tool added to our Private Computing Toolkit. HEIR is an open source compiler that unlocks cryptographically-secure private AI inference.

**Homomorphic encryption**

As new benefits emerge with the growth of AI, balancing privacy and security is top of mind. Standard protections like end-to-end encryption present a trade-off: user-data can be protected from data breaches, but then the service provider cannot provide features that depend on the data, such as spam or virus detection. Critical sectors like healthcare and finance are even more averse to these risks, and strict regulations limit data sharing across institutions. Alternative mechanisms to provide the same features, like local processing, are limited by the capabilities of the local device and the sensitivity of the service provider's IP. Shipping proprietary AI to a device risks leaking the model.

A solution to these issues is [homomorphic encryption](https://en.wikipedia.org/wiki/Homomorphic_encryption), a rapidly maturing technology that fundamentally alters this trade-off by allowing computations to be performed directly on encrypted data. Servers can process ciphertexts and return encrypted results without exposing any underlying information. For example, a cloud service can provide content recommendations without being able to see the user's features. This is no exaggeration: one of the demos featured in this post does exactly this. But while homomorphic encryption has a nontrivial cost overhead, it shifts the capability/privacy trade-off to a question of cost. And the cost of homomorphic encryption is rapidly decreasing.

Google’s history of innovations in privacy technology—from [differential privacy](https://developers.googleblog.com/sharing-our-latest-differential-privacy-milestones-and-advancements/) and [private set membership](https://security.googleblog.com/2021/10/protecting-your-device-information-with.html) to [private information retrieval](https://research.google/pubs/private-join-and-compute-from-pir-with-default/) and [secure enclaves on Google Cloud](https://cloud.google.com/blog/products/identity-security/verifiable-trust-in-the-ai-era-whats-new-in-confidential-computing)—has always focused on securing user data. Homomorphic encryption is another powerful tool we're adding to our private computing toolkit. Like private information retrieval, and in contrast to hardware-based solutions, homomorphic encryption's strong security and privacy guarantees are purely cryptographic. However, manually converting an existing program to use homomorphic encryption efficiently requires a team of cryptographers.

**About HEIR**

To overcome the usability challenges and advance the opportunity homomorphic encryption provides, researchers and engineers at Google built the [HEIR compiler project](https://heir.dev/). HEIR (Homomorphic Encryption Intermediate Representation) is an open-source compiler toolchain and development platform for homomorphic encryption. In particular, HEIR can convert pre-trained AI models that operate on unencrypted data to operate on encrypted inputs. Our vision is to make HEIR a one-click solution to enable non-experts to incorporate encrypted inference into production applications.

Since announcing [our intentions in 2023](https://developers.googleblog.com/expanding-our-fully-homomorphic-encryption-offering/), we’ve seen the homomorphic encryption community embrace HEIR. We have partnered with companies developing hardware accelerators for homomorphic encryption, including [Belfort](http://belfortlabs.com/), [Niobium](https://niobium.co/), [Cornami](https://cornami.com/), and [Optalysys](https://optalysys.com/). The fruits of those efforts are shown in our demos below, and we plan to demonstrate the latency benefits of these accelerators in the near future. HEIR has also become a productive research platform. By building on HEIR, cryptographers can focus on their specific optimization and use the existing infrastructure for testing, benchmarking, and comparisons. This has resulted in collaborations with Georgia Tech, Carnegie Mellon, UC Santa Barbara, Illinois Institute of Technology, Purdue, the University of Edinburgh, Tsinghua University, and others. To date, four peer-reviewed publications were built on HEIR, with more in preparation, and HEIR has accumulated [numerous citations](https://scholar.google.com/scholar?cites=12766019067493592557&as_sdt=5,44&sciodt=0,44&hl=en).

**Applications of HEIR**

To demonstrate how far homomorphic encryption has come, we’re sharing four private inference applications. Each application was compiled with HEIR, and latency numbers are presented for a single-threaded CPU. The source code for all examples is available in our [GitHub repository](https://github.com/google/fully-homomorphic-encryption).

- A [**Deep Learning Recommendation Model**](https://arxiv.org/abs/2506.18150) unlocks serving private content recommendations, joint work with [Belfort Labs](https://belfortlabs.com/), [LG](https://www.google.com/aclk?sa=L&ai=DChsSEwj774ej-8OVAxVHMq0GHYrgEvYYACICCAEQARoCcHY&ae=2&co=1&ase=2&gclid=CjwKCAjw6rfSBhAqEiwA_yocpto3OXAYtmJgE2sj_OVrCTBv1sLvUvCqwAouWQ1Si4xSTKAttoXNExoCzNsQAvD_BwE&cid=CAASWeRoGit-VQ-9xkqb08LHIeyLU4ac_3nU5t8sCtjwDhtyvQb4E1lzzK1LjRlb50mVjSXxUJPXm_Gu3NsZkFxy_opiQpU1cV60l-ZF41gccoSQ7go3Z63Iyac7&cce=2&category=acrcp_v1_71&sig=AOD64_3EzJmrtHthiFCgBjWnwZfKS5hIGQ&q&nis=4&adurl&ved=2ahUKEwiU9f-i-8OVAxWNCDQIHeM_PNcQ0Qx6BAgQEAE), and [New York University](https://engineering.nyu.edu/faculty/brandon-reagen).
- **Credit card fraud detection:** Together with [Niobium](https://niobium.co/) and [hardshell.ai](http://hardshell.ai/), we compiled a credit card fraud detector.
- **Threat intrusion:** Together with [Niobium](https://niobium.co/) we compiled the [Kitsune](https://arxiv.org/abs/1802.09089) system for anomaly detection of encrypted network traffic. This allows a service provider to detect anomalies without revealing the contents of network packets to the service provider.
- **Hotword Detector:** Together with [Belfort Labs](https://belfortlabs.com/) we compiled a hotword detection model, which could allow an audio-triggered AI agent to recognize hotwords while protecting the privacy of the audio recordings.

As the software industry adapts to security and privacy changes amid AI, our research team is working to make homomorphic encryption, easy to develop, fast to run, and ubiquitous across industry.

POSTED IN:

## Related stories

[Security\\
**The Evolving Role of the Red Team in the Era of Agentic Security** \\
\\
At Google, our Red Teams have always operated on the cutting edge of security. We’ve shared our journey in the past: from the high-stakes operations showcased in our Hac…\\
\\
By\\
\\
\\
Daniel Fabian](https://blog.google/security/the-evolving-role-of-the-red-team-in-the-era-of-agentic-security/)

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