---
title: "Introducing AgentKit"
vendor: openai
source_url: https://openai.com/index/introducing-agentkit/
published_at: 2025-10-06T00:00:00.000Z
crawled_at: 2026-05-23T14:44:14.000Z
word_count: 1200
reading_time_minutes: 6
tags: [agents, developer-tools, SDK, OpenAI]
---

October 6, 2025

# Introducing AgentKit

New tools for building, deploying, and optimizing agents.

Today we're launching AgentKit, a complete set of tools for developers and enterprises to build, deploy, and optimize agents. Until now, building agents meant juggling fragmented tools—complex orchestration with no versioning, custom connectors, manual eval pipelines, prompt tuning, and weeks of frontend work before launch. With AgentKit, developers can now design workflows visually and embed agentic UIs faster using new building blocks like:

- **Agent Builder:** a visual canvas for creating and versioning multi-agent workflows
- **Connector Registry:** a central place for admins to manage how data and tools connect across OpenAI products
- **ChatKit:** a toolkit for embedding customizable chat-based agent experiences in your product

We're also expanding evaluation capabilities with new features like datasets, trace grading, automated prompt optimization, and third-party model support to measure and improve agent performance.

Since releasing the Responses API and Agents SDK in March, we've seen developers and enterprises build end-to-end agentic workflows for deep research, customer support, and more. Klarna built a support agent that handles two-thirds of all tickets and Clay 10x'ed growth with a sales agent. AgentKit builds on the Responses API to help developers build agents more efficiently and reliably.

## Design workflows with Agent Builder

As agent workflows grow more complex, developers need clearer visibility into how they work. Agent Builder provides a visual canvas for composing logic with drag-and-drop nodes, connecting tools, and configuring custom guardrails. It supports preview runs, inline eval configuration, and full versioning—ideal for fast iteration.

Builders can get started with a blank canvas or with prebuilt templates.

At Ramp, the team went from a blank canvas to a buyer agent in just a few hours: "Agent Builder transformed what once took months of complex orchestration, custom code, and manual optimizations into just a couple of hours."

Similarly, LY Corporation built a work assistant agent with Agent Builder in less than two hours.

We're also launching a Connector Registry for enterprises to govern and maintain data across multiple workspaces and organizations. The Connector Registry consolidates data sources into a single admin panel across ChatGPT and the API.

## Embed agentic chat experiences with ChatKit

Deploying chat UIs for agents can be surprisingly complex. ChatKit makes it simple to embed chat-based agents that feel native to your product. It can be embedded into apps or websites and customized to match your theme or brand.

Canva said: "We saved over two weeks of time building a support agent for our Canva Developers community with ChatKit, and integrated it in less than an hour."

## Measure agent performance with new Evals capabilities

Building reliable, production-ready agents requires rigorous performance evaluations. OpenAI is adding four new capabilities: Datasets, Trace grading, Automated prompt optimization, and Third-party model support.

## Push agent performance with reinforcement fine-tuning

Reinforcement fine-tuning (RFT) lets developers customize reasoning models. It is generally available on OpenAI o4-mini and in private beta for GPT-5. Two new features in the RFT beta: Custom tool calls and Custom graders.

## Pricing & availability

Starting today, ChatKit and the new Evals capabilities are generally available. Agent Builder is available in beta, and Connector Registry is beginning its beta rollout.

We plan to add a standalone Workflows API and agent deployment options to ChatGPT soon.
