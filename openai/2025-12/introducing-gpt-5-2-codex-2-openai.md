---
title: "Introducing GPT-5.2-Codex"
vendor: openai
source_url: https://openai.com/index/gpt-5-2-codex/
published_at: 2025-12-18T00:00:00.000Z
crawled_at: 2026-05-23T14:59:27.000Z
word_count: 2800
reading_time_minutes: 14
tags: [coding, agents, cybersecurity, codex, software-engineering]
---

# Introducing GPT-5.2-Codex

The most advanced agentic coding model for professional software engineering and defensive cybersecurity.

Today we're releasing GPT-5.2-Codex, the most advanced agentic coding model yet for complex, real-world software engineering. GPT-5.2-Codex is a version of GPT-5.2 further optimized for agentic coding in Codex, including improvements on long-horizon work through context compaction, stronger performance on large code changes like refactors and migrations, improved performance in Windows environments, and significantly stronger cybersecurity capabilities.

As our models continue to advance along the intelligence frontier, we've observed that these improvements also translate to capability jumps in specialized domains such as cybersecurity. For example, just last week, a security researcher using GPT-5.1-Codex-Max with Codex CLI found and responsibly disclosed a vulnerability in React that could lead to source code exposure.

GPT-5.2-Codex has stronger cybersecurity capabilities than any model we've released so far. These advances can help strengthen cybersecurity at scale, but they also raise new dual-use risks that require careful deployment. While GPT-5.2-Codex does not reach a 'High' level of cyber capability under our Preparedness Framework, we're designing our deployment approach with future capability growth in mind.

We're releasing GPT-5.2-Codex today in all Codex surfaces for paid ChatGPT users, and working towards safely enabling access to GPT-5.2-Codex for API users in the coming weeks.

### Pushing the frontier on real-world software engineering

GPT-5.2-Codex builds on GPT-5.2's strengths in professional knowledge work and GPT-5.1-Codex-Max's frontier agentic coding and terminal-using capabilities. GPT-5.2-Codex is now better at long-context understanding, reliable tool calling, improved factuality, and native compaction, making it a more dependable partner for long running coding tasks, while remaining token-efficient in its reasoning.

GPT-5.2-Codex achieves state-of-the-art performance on SWE-Bench Pro (56.4%) and Terminal-Bench 2.0 (64.0%), benchmarks designed to test agentic performance on a wide variety of tasks in realistic terminal environments. It is also much more effective and reliable at agentic coding in native Windows environments.

With these improvements, Codex is more capable at working in large repositories over extended sessions with full context intact. It can more reliably complete complex tasks like large refactors, code migrations, and feature builds—continuing to iterate without losing track, even when plans change or attempts fail.

### Advancing the cyber frontier

When charting performance on one of our core cybersecurity evaluations over time, we see a sharp jump in capability starting with GPT-5-Codex, another large jump with GPT-5.1-Codex-Max and now a third jump with GPT-5.2-Codex. We expect that upcoming AI models will continue on this trajectory.

On December 11, 2025, the React team published three security vulnerabilities affecting apps built with React Server Components. A security researcher using GPT-5.1-Codex-Max with Codex CLI, while attempting to reproduce a different critical React vulnerability (React2Shell, CVE-2025-55182), discovered previously unknown vulnerabilities. These were responsibly disclosed to the React team.

This demonstrates how advanced AI systems can materially accelerate defensive security work in widely used, real-world software. At the same time, capabilities that help defenders move faster can also be misused by bad actors.

### Empowering cyberdefense through trusted access

Security teams can run into restrictions when attempting to emulate threat actors, analyze malware to support remediation, or stress test critical infrastructure. We are developing a trusted access pilot to remove that friction for qualifying users and organizations and enable trusted defenders to use frontier AI cyber capabilities to accelerate cyberdefense.

### Conclusion

GPT-5.2-Codex represents a step forward in how advanced AI can support real-world software engineering and specialized domains like cybersecurity—helping developers and defenders tackle complex, long-horizon work, and strengthening the tools available for responsible security research.
