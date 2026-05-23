---
title: "Networking at the Heart of AI — @Scale: Networking 2025 Recap"
vendor: meta
source_url: https://engineering.fb.com/2025/09/26/networking-traffic/networking-at-the-heart-of-ai-scale-networking-2025-recap/
published_at: 2025-09-26T16:00:52.000Z
crawled_at: 2026-05-23T16:25:41.000Z
word_count: 734
reading_time_minutes: 4
tags: [networking, ai-infrastructure, gpu-clusters, scale-networking, meta]
---

AI is everywhere and, as network engineers, we are right in the thick of it: building the network infrastructure for AI. This year, at our largest @Scale:Networking ever, engineers from Meta, ByteDance, Google, Microsoft, Oracle, AMD, Broadcom, Cisco, and NVIDIA came together to share our latest experiences in architecting, designing, operating, and debugging our AI networks. It's clear what an important role the network has had so far in enabling our large-scale AI advances. Looking forward, we are enabling and defining the future of AI with our networking.

## Setting Context: Rapid Changes and Evolution

Given AI continues to drive so much innovation in networking and general infrastructure, we once again focused @Scale: Networking on AI networking, sharing the new insights and progress in the field. In this past year, we've seen two important trends:

### AI Infra on the Center Stage

Across the industry, AI companies are planning hundreds of billions of dollars of infrastructure build over the next several years. At Meta, this meant investing in building our gigawatt-scale clusters like Prometheus and Hyperion, providing clean and renewable power, and laying the largest transoceanic fiber cable systems in the world to ensure billions across the globe have access to all this AI innovation.

### The Models and the Primary AI Workloads Are Rapidly Evolving

We've focused a lot over the last several years on the requirements of large-scale, foundational training. At Meta, we went from 4K to 24K to 129K-GPU clusters based on Ethernet/RoCE in less than two years, tackling new challenges in high performance and high reliability with each leap. Now, in the last 9-12 months, we've seen a rapid expansion of workloads that include mixture-of-experts, reasoning models, reinforcement learning, post-training, synthetic data generation, distributed inference, and more. All of these have different network requirements, and they are all now part of our challenge.

## The Role of the Network in AI

### The Network Is the Computer

Between the rapidly changing AI workloads and massive physical infrastructure builds, the network plays the interface role of abstracting the underlying infrastructure as much as possible to the workloads. From the model perspective, the infrastructure should look like one gigantic GPU, and the network is key to this abstraction.

### Co-Designing the Network With the AI Stack

Achieving this abstraction goal requires addressing challenges like varying distances and bandwidths (especially in the scale-up and scale-out domains), and hardware variety across different accelerators, NICs, and fabrics. It's a full-stack/end-to-end problem for networking, bringing to bear all our experience in NICs, routing, and congestion control, and tuning all these closely with the GPU-based stack.

### Reliability Is Key

Not only do we have to provide the performance and ease-of-use the models expect, but we also must operate this infrastructure with high reliability, finding and quickly reacting to those failures seamlessly.

### Innovation and Optionality

Going forward, we need to continually innovate to stay ahead and provide optionality, as we expect constant change above us in the models/workloads and below us in the rest of the infrastructure. We want a network stack that blends the best of high performance computing's capabilities with open and scalable distributed system principles, ensuring we're ready for whatever comes next.

## More from @Scale:Networking 2025

Please visit the @Scale YouTube channel to check out all the talks from this year's Networking @Scale. Meta continually organizes all the @Scale events (Systems & Reliability, AI & Data, and the upcoming Product in October) so our communities can share the innovations and challenges we're tackling and can learn from each other.

We had a variety of talks with live Q&As with two major themes:

1. **Underlying physical network infrastructure talks**: switch topologies and control plane, NIC and host networking, and scalable operations/high reliability.
2. **Higher-layer, model-oriented talks**: parallelism design, job-level debuggability, scaling for large pre-training, and handling new use cases in reinforcement learning, mixture of experts, and inference.

From the perspective of what's coming in the future for AI and networking, we had keynotes from Meta and Microsoft and a vendor panel with key GPU and network ASIC vendors.

We thank again everyone from Meta, ByteDance, Google, Microsoft, Oracle, AMD, Broadcom, Cisco, and NVIDIA who worked with us to share all of their latest learnings with the community. We look forward to what promises to be another rapid year of network and AI innovation that we'll cover at the next @Scale: Networking in 2026!