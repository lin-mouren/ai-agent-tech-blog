---
title: "Confidential Inference via Trusted Virtual Machines"
vendor: anthropic
source_url: https://www.anthropic.com/research/confidential-inference-trusted-vms
published_at: 2025-06-18T00:00:00.000Z
crawled_at: 2026-05-23T14:11:22.000Z
word_count: 1580
reading_time_minutes: 8
tags: [security, confidential-computing, research, privacy]
---

Announcements

# Confidential Inference via Trusted Virtual Machines

Jun 18, 2025

[Read the paper](https://assets.anthropic.com/m/c52125297b85a42/original/Confidential_Inference_Paper.pdf)

Every day, millions of users entrust Claude with sensitive information—from proprietary code to confidential business strategies. At Anthropic, we're researching and building new technology to ensure that our users' trust is warranted—and in fact, to ensure that their trust is cryptographically guaranteed.

What do we mean by "cryptographically guaranteed"? In a new report published in collaboration with Pattern Labs, we describe the mechanics of Confidential Inference. Confidential Inference is a set of tools we can use to process encrypted data and to show that such data is only readable within servers that can prove themselves trustworthy. There are two main reasons to adopt these tools:

- Model Weight Security: We can use Confidential Inference as one component of our broader effort to secure frontier models like Claude against increasingly capable threat actors;
- User Security: We can use Confidential Inference to prove that sensitive user data is kept private.

## Inference service

The guiding principle behind Confidential Inference is that sensitive data should remain encrypted except at the point where it's processed. To enforce this, we use the established methods of confidential computing. This means we build a chain of trust that attests to the security of our software, and then use that attestation to enforce rules about exactly which software is allowed to use the encryption keys.

For user data, there are two points where we need to operate on the sensitive cleartext:

- The API Server handles a prompt, transforms it into tokens, and operates most of the logic behind a Claude API request;
- The Inference Server runs the "brains" of Claude on hardware accelerators to generate completion tokens from the prompt.

For model weights, only the Inference Server receives sensitive data.

We're working on a system based on this design for our own implementation. For this implementation, the majority of our Inference Server runs on the "untrusted" side—where it might change frequently, but where changes cannot affect the security of the system as a whole. We have a small trusted loader, running on a separate virtual machine isolated by the hypervisor.

## Trusted environment

The report describes the loader running in a confidential computing environment with:
1. Encrypted memory, isolated by hardware from other workloads;
2. Disabled debugging features;
3. Cryptographic proof that the correct code is being run.

## Future directions

As frontier models grow more capable, we may find it necessary to incorporate further safeguards at the secure loader layer. This may include features such as an additional layer of egress bandwidth limitations on servers that holds cleartext model weights, or requiring a signature from a safety classifier in order to run inference.

## Conclusions

This research will advance our ongoing efforts to secure our model weights and protect user data. Using this model to protect a user request is designed to ensure that customer data is only ever decrypted in contexts with enhanced hardware-based security controls.

Hardware designers should consider incorporating confidential computing into their chips. If there is a hardware root of trust attached to the accelerator, then the trust boundary of this kind of system can be significantly reduced.

[Read the full report](https://assets.anthropic.com/m/c52125297b85a42/original/Confidential_Inference_Paper.pdf)