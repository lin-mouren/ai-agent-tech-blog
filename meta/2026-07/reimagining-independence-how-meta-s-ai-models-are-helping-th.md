---
title: "Reimagining Independence: How Meta’s AI Models Are Helping the University of Pittsburgh Transform Assistive Robotics"
vendor: meta
source_url: https://ai.meta.com/blog/assistive-robotics-university-of-pittsburgh-sam-dino/
published_at: 2026-07-27T13:00:05.065Z
crawled_at: 2026-07-28T02:00:45.079Z
word_count: 1735
reading_time_minutes: 9
tags: [llama, multimodal, safety, infrastructure, evaluation, api, open-source]
---

[Go up one level](https://ai.meta.com/blog/assistive-robotics-university-of-pittsburgh-sam-dino/# "Go up one level") [](https://ai.meta.com/)

- [Products](https://ai.meta.com/blog/assistive-robotics-university-of-pittsburgh-sam-dino/#)

- [AI Research](https://ai.meta.com/blog/assistive-robotics-university-of-pittsburgh-sam-dino/#)

- [Resources](https://ai.meta.com/blog/assistive-robotics-university-of-pittsburgh-sam-dino/#)

- [About](https://ai.meta.com/blog/assistive-robotics-university-of-pittsburgh-sam-dino/#)

- [AI Developers](https://developer.meta.com/ai/?utm_source=ai_meta_site&utm_medium=web&utm_campaign=nav_AI-developers_07242026&utm_content=nav_AI-developers)


- [Try Meta AI](https://applink.meta.ai/?pt=10684&pid=ai_meta_site&utm_source=ai_meta_site&utm_medium=web&utm_campaign=nav_try-meta-ai-palette_07072026&utm_content=nav_try-meta-ai-palette_07072026&ct=nav_try-meta-ai-palette_07072026&referrer=utm_source%3Dai_meta_site%26utm_medium%3Dweb%26utm_campaign%3Dnav_try-meta-ai-palette_07072026%26utm_content%3Dnav_try-meta-ai-palette_07072026)
- [Toggle site search](https://ai.meta.com/blog/assistive-robotics-university-of-pittsburgh-sam-dino/# "Toggle site search")


[Close submenu](https://ai.meta.com/blog/assistive-robotics-university-of-pittsburgh-sam-dino/# "Close submenu") [Main menu](https://ai.meta.com/blog/assistive-robotics-university-of-pittsburgh-sam-dino/# "Main menu")

[BACK](https://ai.meta.com/blog/assistive-robotics-university-of-pittsburgh-sam-dino/# "Go up one level")

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
>](https://ai.meta.com/blog/assistive-robotics-university-of-pittsburgh-sam-dino/#)

- [AI Research\\
\\
>](https://ai.meta.com/blog/assistive-robotics-university-of-pittsburgh-sam-dino/#)

- [Resources\\
\\
>](https://ai.meta.com/blog/assistive-robotics-university-of-pittsburgh-sam-dino/#)

- [About\\
\\
>](https://ai.meta.com/blog/assistive-robotics-university-of-pittsburgh-sam-dino/#)

- [AI Developers](https://developer.meta.com/ai/?utm_source=ai_meta_site&utm_medium=web&utm_campaign=nav_AI-developers_07242026&utm_content=nav_AI-developers)

[Try Meta AI](https://applink.meta.ai/?pt=10684&pid=ai_meta_site&utm_source=ai_meta_site&utm_medium=web&utm_campaign=nav_try-meta-ai-palette_07072026&utm_content=nav_try-meta-ai-palette_07072026&ct=nav_try-meta-ai-palette_07072026&referrer=utm_source%3Dai_meta_site%26utm_medium%3Dweb%26utm_campaign%3Dnav_try-meta-ai-palette_07072026%26utm_content%3Dnav_try-meta-ai-palette_07072026)

Open Source

# Reimagining Independence: How Meta’s AI Models Are Helping the University of Pittsburgh Transform Assistive Robotics

July 27, 2026•

8 minute read



In the heart of Pittsburgh, a quiet revolution is underway — one that promises to redefine what independence means for people with disabilities. At the center of this movement is the [Human Engineering Research Laboratories (HERL)](https://www.herl.pitt.edu/), a pioneering institute at the University of Pittsburgh, now leading an initiative with up to $41.5 million in funding from the [Advanced Research Projects Agency for Health (ARPA-H)](https://arpa-h.gov/), a US research funding agency established to support transformative biomedical and health breakthroughs. With support from ARPA-H, the HERL team and [ATDev](https://assistivetech.dev/), a pioneer in innovative assistive technology, are building the Robotic Assistive Mobility and Manipulation Platform Providing Independence for People with Disabilities (RAMMP), blending cutting-edge robotics, artificial intelligence, and user-centered design.

For the estimated [5.5 million wheelchair users in the United States](https://www.volpe.dot.gov/news/us-dot-volpe-center-human-factors-study-informs-rule-air-travelers-disabilities), preservation of mobility ensures individual opportunity and participation in everyday life. When assistive technology does not reflect the complexity of the real world, it can undermine confidence, independence, and physical safety. The statistics are sobering: over [100,000 wheelchair-related injuries are treated in US emergency departments each year](https://www.pittwire.pitt.edu/features-articles/2025/11/04/advanced-research-projects-agency-health-rammp-herl), often due to trips and falls. As a result, the need for smarter, safer, and more adaptable technology is urgent.

RAMMP: A New Era for Assistive Mobility

The ARPA-H-supported Robotic Assistive Mobility and Manipulation Platform ( [RAMMP](https://arpa-h.gov/explore-funding/awards/2771)) project aims to address the shortcomings in current robotic mobility platform design through integration of advanced robotics, novel operating systems, and digital twin technology — creating a virtual simulation environment for safe, scalable testing and development. RAMMP’s approach also integrates artificial intelligence, including the use of several of Meta’s open source AI vision models, including [DINO](https://ai.meta.com/research/dinov3/) and [Segment Anything Model (SAM)](https://ai.meta.com/research/sam3/).

DINO and SAM have already assisted in a variety of projects ranging from those focused on medical imaging to wildlife conservation. DINO, a self-supervised vision transformer, excels at learning visual representations from unlabeled data, making it ideal for environments where annotated datasets are scarce. SAM, on the other hand, is designed to “segment anything” and has the ability to identify and outline any object in an image or video with minimal prompting. Segment Anything’s versatility and accuracy have made it a foundational tool in domains where precise object recognition is paramount.

Engineering for the Real World: Running DINOv3 and SAM on Edge Devices

For people relying on assistive devices, every second counts. The unpredictable nature of everyday environments, such as a child darting across a sidewalk, the sudden appearance of a curb, or a dropped set of keys, requires an immediate reaction. Processing camera images and sensor data directly on the device, known as edge computing, empowers robotic mobility platforms to function as responsive tools. These tools must be robust and consistent across the wide range of dynamic environments in which people live.

At the same time, deploying powerful AI models like DINOv3 and SAM on limited, battery-powered hardware presents significant engineering challenges. Real-world deployments must consider practical factors, including battery life, heat dissipation, unreliable network connectivity, and strict size and weight requirements.

However, overcoming these constraints mean nothing to the end user if they can't perform their activities of daily living using these new robotic systems. These newer methods allow users to interact with the robot more naturally, using their immediate surroundings as context, freeing both engineers and users from having to design and navigate complex, time-consuming interfaces. The ability to use natural language combined with image data to query the user’s and robot’s environment and provide more direct commands directly reduces the cognitive load and amount of context switching required for a user to do something as simple as picking up a cup off a table.

This functionality is already being integrated by the RAMMP team into their first prototype. Leveraging tools built off of DINO to enable querying the robot’s image sensors to detect automatic door buttons, cups, and curbs/ground for navigation assistance. With this functionality now ready for real-world testing, engineers are focusing on voice and touch input, letting users select and interact with specific objects in their surroundings. In addition to the existing challenges of ensuring accuracy and temporal coherence of the model outputs, this provides the additional challenge of ensuring robustness and predictability across user prompts and inputs.

DINOv3 serves as a compact, efficient 'visual brain' for devices — a general-purpose foundation on which task-specific, lightweight modules can be layered for actions such as object detection or movement tracking, enabling reuse of visual data and conserving power.

Applying both models as part of the development of robotics systems, engineers optimize models for edge devices, reducing memory footprint, using lower precision when appropriate, and deploying in formats tailored for real-world conditions. This ensures reliable, real-time operation for users. By running at practical resolutions and with efficient batching, both models stay fast and dependable, even on the compact, battery-powered hardware used in robotic mobility platforms and robotic arms, — sometimes trading a little bit of boundary precision and/or feature detail for the speed and stability needed by users on the go. This balance between precision and practicality is central to the project's philosophy.

“For assistive robotics, performance is not measured by benchmark accuracy alone, but by whether a system can operate reliably in the unpredictability of everyday life," said Sivashankar Sivakanthan, Chief of Staff to the RAMMP project. “Running models like DINOv3 and SAM on-device is what enables real-time perception that users can trust - without relying on connectivity or compromising safety.”

RAMMP's perception system is built on RF-DETR, a lightweight detection model fine-tuned with DINOv2 embeddings. Training data is auto-labeled using SAM, enabling the team to rapidly generate high-quality annotations across the full range of angles, heights, backgrounds, and lighting situations that assistive devices encounter in the real world. Data augmentations and multi-view strategies further enforce consistency across perspectives. The result is a system that is smart, adaptive, and offers safer and more confident mobility.

By combining SAM's labeling power with DINOv2's rich visual representations in a fine-tuned RF-DETR model, RAMMP achieves real-time 360-degree environmental awareness and adaptive object detection.

A Collaborative Vision for the Future

HERL and ATDev are working together as key partners within the RAMMP consortium, each bringing distinct strengths to the project. HERL leads the initiative with its deep expertise in biomedical engineering and user-centered research, setting the vision for next-generation assistive mobility. ATDev brings a robust engineering perspective, taking HERL's translational research and making it function in real-world devices. Together, HERL and ATDev exemplify how academic leadership and technical innovation can combine to create mobility solutions that are both groundbreaking and deeply attuned to the lived experience of users.

In addition to integration of cutting-edge artificial intelligence, HERL’s approach is deeply collaborative, engaging wheelchair users, clinicians, and advocacy groups throughout the design process. This participatory action methodology ensures that technology addresses real-world needs, not just hypothetical ones. The national consortium behind RAMMP includes partners like Kinova Robotics, LUCI Mobility, ATDev, and academic leaders at Carnegie Mellon, Cornell, Northeastern, and Purdue.

“Through RAMMP, ARPA-H aims to create a future where Americans with limited mobility can more easily live independently, pursue work, and enjoy leisure activities by leveraging advanced robotics,” said [Mansoor Khan](https://arpa-h.gov/about/people/mansoor-khan), ARPA-H Program Manager. “Meta’s vision models are a critical technology that allows the robotics platform to ‘see.’ These models help the robot understand the scene, navigate the world, and pick up the right objects — significantly reducing user cognitive burden and increasing independence.”

Beyond enhancing individual mobility, RAMMP aims to catalyze new workforce and manufacturing opportunities in Pittsburgh and across Pennsylvania, fostering advanced mobility solutions and domestic production. This vision weaves technological progress with economic and social advancement.

“What the RAMMP team is building through ARPA-H is a glimpse of what American health innovation looks like when we stop accepting the status quo,” said [Alicia Jackson, Ph.D.](https://arpa-h.gov/about/people/alicia-jackson), ARPA-H Director. “Millions of Americans with limited mobility deserve technology that meets them where they are, not technology that asks them to adapt. Partnering with world-class innovators like Meta to bring frontier AI into assistive robotics is how we make that happen faster than anyone thought possible."

Looking ahead, the RAMMP team will continue to advance the integration of next-generation perception models, including SAM 3.1 and DINOv3, to further improve real-time environmental understanding and interaction. Future work will focus on strengthening temporal consistency, robustness across diverse real-world conditions, and tighter integration with decision-making and control systems. By combining these advances, RAMMP aims to move toward assistive systems that not only perceive their environment accurately, but also adapt over time to the unique needs, behaviors, and contexts of each user. The next generation of assistive robotics will not just move people — it will move society closer to a world where everyone, regardless of ability, can participate fully and independently.

[Learn More About DINO](https://ai.meta.com/research/dinov3/)

[Learn More About SAM](https://ai.meta.com/research/sam3/)

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