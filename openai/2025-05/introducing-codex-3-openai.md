---
title: "Introducing Codex"
vendor: openai
source_url: https://openai.com/index/introducing-codex/
published_at: 2025-05-16T00:00:00.000Z
crawled_at: 2026-05-23T16:40:00.000Z
word_count: 1434
reading_time_minutes: 7
tags: [codex, code-engineering-agent, o3, developer-tools, ai-agents, software-engineering]
---

# Introducing Codex

A cloud-based software engineering agent that can work on many tasks in parallel, powered by codex-1. Available to ChatGPT Pro, Business, and Enterprise users today, and Plus users soon.

*Update on June 3, 2025: Codex is now available to ChatGPT Plus users. We're also enabling users to provide Codex with internet access during task execution.*

---

Today we're launching a research preview of Codex: a cloud-based software engineering agent that can work on many tasks in parallel. Codex can perform tasks for you such as writing features, answering questions about your codebase, fixing bugs, and proposing pull requests for review; each task runs in its own cloud sandbox environment, preloaded with your repository.

Codex is powered by codex-1, a version of OpenAI o3 optimized for software engineering. It was trained using reinforcement learning on real-world coding tasks in a variety of environments to generate code that closely mirrors human style and PR preferences, adheres precisely to instructions, and can iteratively run tests until it receives a passing result. We're starting to roll out Codex to ChatGPT Pro, Enterprise, and Business users today, with support for Plus and Edu coming soon.

## How Codex works

Today you can access Codex through the sidebar in ChatGPT and assign it new coding tasks by typing a prompt and clicking "Code". If you want to ask Codex a question about your codebase, click "Ask". Each task is processed independently in a separate, isolated environment preloaded with your codebase. Codex can read and edit files, as well as run commands including test harnesses, linters, and type checkers. Task completion typically takes between 1 and 30 minutes, depending on complexity, and you can monitor Codex's progress in real time.

Once Codex completes a task, it commits its changes in its environment. Codex provides verifiable evidence of its actions through citations of terminal logs and test outputs, allowing you to trace each step taken during task completion. You can then review the results, request further revisions, open a GitHub pull request, or directly integrate the changes into your local environment. In the product, you can configure the Codex environment to match your real development environment as closely as possible.

Codex can be guided by AGENTS.md files placed within your repository. These are text files, akin to README.md, where you can inform Codex how to navigate your codebase, which commands to run for testing, and how best to adhere to your project's standard practices. Like human developers, Codex agents perform best when provided with configured dev environments, reliable testing setups, and clear documentation.

On coding evaluations and internal benchmarks, codex-1 shows strong performance even without AGENTS.md files or custom scaffolding. On SWE-Bench Verified, codex-1 achieves 58.2% resolution rate (at 192k context, medium reasoning effort).

## Building safe and trustworthy agents

We're releasing Codex as a research preview, in line with our iterative deployment strategy. We prioritized security and transparency when designing Codex so users can verify its outputs — a safeguard that grows increasingly more important as AI models handle more complex coding tasks independently and safety considerations evolve. Users can check Codex's work through citations, terminal logs and test results. When uncertain or faced with test failures, the Codex agent explicitly communicates these issues, enabling users to make informed decisions about how to proceed. It still remains essential for users to manually review and validate all agent-generated code before integration and execution.

### Preventing abuse

Safeguarding against malicious applications of AI-driven software engineering, such as malware development, is increasingly critical. At the same time, it's important that protective measures do not unduly hinder legitimate and beneficial applications that may involve techniques sometimes also used for malware development, such as low level kernel engineering.

To balance safety and utility, Codex was trained to identify and precisely refuse requests aimed at development of malicious software, while clearly distinguishing and supporting legitimate tasks. We've also enhanced our policy frameworks and incorporated rigorous safety evaluations to reinforce these boundaries effectively. We've published an addendum to the o3 System Card to reflect these evaluations.

### Secure execution

The Codex agent operates entirely within a secure, isolated container in the cloud. During task execution, internet access is disabled, limiting the agent's interaction solely to the code explicitly provided via GitHub repositories and pre-installed dependencies configured by the user via a setup script. The agent cannot access external websites, APIs, or other services.

## Aligning to human preferences

A primary goal while training codex-1 was to align outputs closely with human coding preferences and standards. Compared to OpenAI o3, codex-1 consistently produces cleaner patches ready for immediate human review and integration into standard workflows.

In head-to-head evaluations on SWE-Bench Verified, codex-1 produces more concise and directly applicable patches compared to base o3, reducing the need for additional human editing before PR submission.

## Early use cases

Technical teams at OpenAI have started using Codex as part of their daily toolkit. It is most often used by OpenAI engineers to offload repetitive, well-scoped tasks, like refactoring, renaming, and writing tests, that would otherwise break focus. It's equally useful for scaffolding new features, wiring components, fixing bugs, and drafting documentation. Teams are building new habits around it: triaging on-call issues, planning tasks at the start of the day, and offloading background work to keep moving.

Leading up to release, we've also been working with a small group of external testers:

- **Cisco** is exploring how Codex can help their engineering teams bring ambitious ideas to life faster. As early design partners, Cisco is helping shape the future of Codex by evaluating it for real-world use cases across their product portfolio.
- **Temporal** uses Codex to accelerate feature development, debug issues, write and execute tests, and refactor large codebases. It also helps them stay focused by running complex tasks in the background.
- **Superhuman** uses Codex to speed up small but repetitive tasks like improving test coverage and fixing integration failures. It also helps them ship faster by enabling product managers to contribute lightweight code changes without pulling in an engineer.
- **Kodiak** is using Codex to help write debugging tools, improve test coverage, and refactor code — accelerating development of the Kodiak Driver, their autonomous driving technology.

## Updates to Codex CLI

Last month, we launched Codex CLI, a lightweight open-source coding agent that runs in your terminal. It brings the power of models like o3 and o4-mini into your local workflow, making it easy to pair with them to complete tasks faster.

Today, we're also releasing a smaller version of codex-1, a version of o4-mini designed specifically for use in Codex CLI. This new model supports faster workflows in the CLI and is optimized for low-latency code Q&A and editing, while retaining the same strengths in instruction following and style. It's available now as the default model in Codex CLI and in the API as codex-mini-latest.

We're also making it much easier to connect your developer account to Codex CLI. Instead of manually generating and configuring an API token, you can now sign in with your ChatGPT account and select the API organization you want to use. Plus and Pro users who sign in to Codex CLI with ChatGPT can also begin redeeming $5 and $50 in free API credits, respectively, for the next 30 days.

## Codex availability, pricing, and limitations

Starting today, we're rolling out Codex to ChatGPT Pro, Enterprise, and Business users globally, with support for Plus and Edu coming soon. Users will have generous access at no additional cost for the coming weeks so you can explore what Codex can do, after which we'll roll out rate-limited access and flexible pricing options.

For developers building with codex-mini-latest, the model is available on the Responses API and priced at $1.50 per 1M input tokens and $6 per 1M output tokens, with a 75% prompt caching discount.

Codex is still early in its development. As a research preview, it currently lacks features like image inputs for frontend work, and the ability to course-correct the agent while it's working. Additionally, delegating to a remote agent takes longer than interactive editing, which can take some getting used to.

## What's next

We imagine a future where developers drive the work they want to own and delegate the rest to agents — moving faster and being more productive with AI. To achieve that, we're building a suite of Codex tools that support both real-time collaboration and asynchronous delegation.

Pairing with AI tools like Codex CLI and others has quickly become an industry norm, helping developers move faster as they code. But we believe the asynchronous, multi-agent workflow introduced by Codex in ChatGPT will become the de facto way engineers produce high-quality code.

Ultimately, we see these two modes of interaction — real-time pairing and task delegation — converging. Developers will collaborate with AI agents across their IDEs and everyday tools to ask questions, get suggestions, and offload longer tasks, all in a unified workflow.

Looking ahead, we plan to introduce more interactive and flexible agent workflows. Developers will soon be able to provide guidance mid-task, collaborate on implementation strategies, and receive proactive progress updates. We also envision deeper integrations across the tools you already use: today Codex connects with GitHub, and soon you'll be able to assign tasks from Codex CLI, ChatGPT Desktop, or even tools such as your issue tracker or CI system.

Software engineering is one of the first industries to experience significant AI-driven productivity gains, opening new possibilities for individuals and small teams. While we're optimistic about these gains, we're also collaborating with partners to better understand the implications of widespread agent adoption on developer workflows, skill development across people, skill levels, and geographies.

This is just the beginning — and we're excited to see what you build with Codex.