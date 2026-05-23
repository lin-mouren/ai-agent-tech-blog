---
title: "From model to agent: Equipping the Responses API with a computer environment | OpenAI"
vendor: openai
source_url: https://openai.com/index/equip-responses-api-computer-environment/
published_at: 2026-03-11T00:00:00.000Z
crawled_at: 2026-05-23T15:30:04.000Z
word_count: 1582
reading_time_minutes: 8
tags: [agents, api, infrastructure, engineering, product]
---

# From model to agent: Equipping the Responses API with a computer environment

By Bo Xu, Danny Zhang, and Rohit Arunachalam

March 11, 2026

We are currently in a shift from using models, which excel at particular tasks, to using agents capable of handling complex workflows. By prompting models, you can only access trained intelligence. However, giving the model a computer environment can achieve a much wider range of use cases, like running services, requesting data from APIs, or generating more useful artifacts like spreadsheets or reports.

OpenAI's Responses API, together with the shell tool and a hosted container workspace, is designed to address practical problems of building agents: where to put intermediate files, how to avoid pasting large tables into a prompt, how to give the workflow network access without creating a security headache.

## The shell tool

The shell tool makes the model dramatically more powerful: it interacts with a computer through the command line to carry out a wide range of tasks. Built on familiar Unix tooling, it can do anything you would expect, with utilities like grep, curl, and awk available out of the box.

## Orchestrating the agent loop

The Responses API can orchestrate between the model and hosted tools out of the box. When the API receives a prompt, it assembles model context: user prompt, prior conversation state, and tool instructions. For shell execution to work, the prompt must mention using the shell tool and the selected model must be trained to propose shell commands - models GPT-5.2 and later are trained for this.

## Compaction

To avoid losing important context as long-running tasks fill the context window, we added native compaction in the Responses API. Our latest models are trained to analyze prior conversation state and produce a compaction item that preserves key prior state in an encrypted token-efficient representation.

## Container context

Inside the container, the model can read files, query databases, and access external systems under network policy controls. We built hosted containers to use a sidecar egress proxy - all outbound network requests flow through a centralized policy layer that enforces allowlists and access controls.

## Agent skills

Agent skills package reusable multi-step patterns into composable building blocks. Concretely, a skill is a folder bundle that includes SKILL.md metadata and instructions plus supporting resources.