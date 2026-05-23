---
title: "Introducing ChatGPT agent: bridging research and action"
vendor: openai
source_url: https://openai.com/index/introducing-chatgpt-agent/
published_at: 2025-07-17T00:00:00.000Z
crawled_at: 2026-05-23T14:18:59.000Z
word_count: 2160
reading_time_minutes: 11
tags: [agents, chatgpt, tool-use, safety]
---

Introducing ChatGPT agent: bridging research and action | OpenAI

July 17, 2025

[Product](https://openai.com/news/product-releases/) [Release](https://openai.com/research/index/release/)

# Introducing ChatGPT agent: bridging research and action

ChatGPT now thinks and acts, proactively choosing from a toolbox of agentic skills to complete tasks for you using its own computer.

ChatGPT can now do work for you using its own computer, handling complex tasks from start to finish.

You can now ask ChatGPT to handle requests like "look at my calendar and brief me on upcoming client meetings based on recent news," "plan and buy ingredients to make Japanese breakfast for four," and "analyze three competitors and create a slide deck." ChatGPT will intelligently navigate websites, filter results, prompt you to log in securely when needed, run code, conduct analysis, and even deliver editable slideshows and spreadsheets that summarize its findings.

At the core of this new capability is a unified agentic system. It brings together three strengths of earlier breakthroughs: Operator's ability to interact with websites, deep research's skill in synthesizing information, and ChatGPT's intelligence and conversational fluency.

ChatGPT carries out these tasks using its own virtual computer, fluidly shifting between reasoning and action to handle complex workflows from start to finish, all based on your instructions.

Most importantly, you're always in control. ChatGPT requests permission before taking actions of consequence, and you can easily interrupt, take over the browser, or stop tasks at any point.

Starting today, Pro, Plus, and Team users can activate ChatGPT's new agentic capabilities directly through the tools dropdown from the composer by selecting 'agent mode' at any point in any conversation.

## A natural evolution of Operator and deep research

Previously, Operator and deep research each brought unique strengths: Operator could scroll, click, and type on the web, while deep research excelled at analyzing and summarizing information. But they worked best in different situations: Operator couldn't dive deep into analysis or write detailed reports, and deep research couldn't interact with websites to refine results or access content requiring user authentication. By integrating these complementary strengths in ChatGPT and introducing additional tools, we've unlocked entirely new capabilities within one model.

## An agent that works for you, with you

We've equipped ChatGPT agent with a suite of tools: a visual browser that interacts with the web through a graphical-user interface, a text-based browser for simpler reasoning-based web queries, a terminal, and direct API access. The agent can also leverage ChatGPT connectors, which allows you to connect apps like Gmail and Github so ChatGPT can find information relevant to your prompts. You can also log in on any website by taking over the browser.

All this is done using its own virtual computer, which preserves the context necessary for the task, even when multiple tools are used — the model can choose to open a page using the text browser or visual browser, download a file from the web, manipulate it by running a command in the terminal, and then view the output back in the visual browser.

ChatGPT agent is designed for iterative, collaborative workflows, far more interactive and flexible than previous models. As ChatGPT works, you can interrupt at any point to clarify your instructions, steer it toward desired outcomes, or change the task entirely.

## Broadening real-world utility

These unified agentic capabilities significantly enhance ChatGPT's usefulness in both everyday and professional contexts. At work, you can automate repetitive tasks, like converting screenshots or dashboards into presentations, rearranging meetings, planning and booking offsites, and updating spreadsheets with new financial data.

The model's elevated capabilities are reflected in its state-of-the-art (SOTA) performance on evaluations measuring web browsing and real-world task completion capabilities.

On Humanity's Last Exam, an evaluation that measures AI's performance across a broad range of subjects on expert-level questions, the model powering ChatGPT agent scores a new pass@1 SOTA at 41.6.

On FrontierMath — the hardest known math benchmark, featuring novel, unpublished problems — ChatGPT agent reaches 27.4% accuracy, outperforming previous models by a wide margin.

On DSBench, designed to evaluate agents on realistic data science tasks, ChatGPT agent notably surpasses human performance by a significant margin.

On SpreadsheetBench, ChatGPT agent outperforms existing models by a significant margin. When given the ability to edit spreadsheets directly, ChatGPT agent scores 45.5%, compared to Copilot in Excel's 20.0%.

On BrowseComp, a benchmark that measures browsing agents' ability to locate hard-to-find information on the web, the model set a new SOTA with 68.9%, 17.4 percentage points higher than deep research.

## How to use

You can activate ChatGPT's new agentic capabilities through the tools dropdown from the composer by selecting 'agent mode' at any point in any conversation. Simply describe your desired task — whether it's conducting deep research, creating a slideshow, or submitting expenses.

## Novel capabilities, novel risks

This release marks the first time users can ask ChatGPT to take actions on the web. This introduces new risks, particularly because ChatGPT agent can work directly with your data. We've strengthened the robust controls from Operator's research preview and added safeguards for challenges such as handling sensitive information on the live web, broader user reach, and (limited) terminal network access.

We've placed a particular emphasis on safeguarding ChatGPT agent against adversarial manipulation through prompt injection. We've trained and tested the agent on identifying and resisting prompt injections, in addition to using monitoring to rapidly detect and respond to prompt injection attacks.

We've also implemented mitigations around model mistakes: explicit user confirmation before actions with real-world consequences, active supervision ("Watch Mode") for critical tasks like sending emails, and proactive risk mitigation for high-risk tasks such as bank transfers.

## Our strongest safety stack yet for biological risk

With the model's increased capabilities, we've made the decision to treat ChatGPT agent as High Biological and Chemical capabilities under our Preparedness Framework, activating the associated safeguards. This model has our most comprehensive safety stack to date with enhanced safeguards for biology: comprehensive threat modeling, dual-use refusal training, always-on classifiers and reasoning monitors, and clear enforcement pipelines.

## Availability

ChatGPT agent starts rolling out today to Pro, Plus, and Team; Pro will get access by the end of day, while Plus and Team users will get access over the next few days. Enterprise and Education users will get access in the coming weeks. Pro users have 400 messages per month, while other paid users get 40 messages monthly.

## Limitations and looking ahead

ChatGPT agent is still in its early stages. It's capable of taking on a range of complex tasks, but it can still make mistakes. While we see significant potential in its ability to generate slideshows, this functionality is currently in beta. We're already training the next iteration of ChatGPT's slideshow creation to produce more polished, sophisticated outputs.