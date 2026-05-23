---
title: "Managing context on the Claude Developer Platform | Claude"
vendor: anthropic
source_url: https://www.anthropic.com/news/context-management?=
published_at: 2025-09-29T14:58:11.000Z
crawled_at: 2026-05-23T09:10:15.268Z
word_count: 2870
reading_time_minutes: 15
tags: [claude, agents, api, product, enterprise]
---

[Home page](https://claude.com/?=)

Explore here



# Managing    context    on    the    Claude    Developer    Platform

Introducing context editing and the memory tool to help developers build more effective agents that handle long-running tasks.

- Category







[Product announcements](https://claude.com/blog/category/announcements?=)

- Product









Claude Platform

- Date



September 29, 2025

- Reading time





5



min

- Share

[Copy link](https://claude.com/blog/context-management?=#)

https://claude.com/blog/context-management


Today, we’re introducing new capabilities for managing your agents’ context on the Claude Developer Platform: context editing and the memory tool.

With our latest model, [Claude Sonnet 4.5](https://www.anthropic.com/news/claude-sonnet-4-5), these capabilities enable developers to build AI agents capable of handling long-running tasks at higher performance and without hitting context limits or losing critical information.

## Context windows have limits, but real work doesn’t

As production agents handle more complex tasks and generate more tool results, they often exhaust their effective context windows—leaving developers stuck choosing between cutting agent transcripts or degrading performance. Context management solves this in two ways, helping developers ensure only relevant data stays in context and valuable insights get preserved across sessions.

**Context editing** automatically clears stale tool calls and results from within the context window when approaching token limits. As your agent executes tasks and accumulates tool results, context editing removes stale content while preserving the conversation flow, effectively extending how long agents can run without manual intervention. This also increases the effective model performance as Claude focuses only on relevant context.



**The memory tool** enables Claude to store and consult information outside the context window through a file-based system. Claude can create, read, update, and delete files in a dedicated memory directory stored in your infrastructure that persists across conversations. This allows agents to build up knowledge bases over time, maintain project state across sessions, and reference previous learnings without having to keep everything in context.

Claude plays Catan: Managing agent context with Sonnet 4.5 - YouTube

Tap to unmute

[Claude plays Catan: Managing agent context with Sonnet 4.5](https://www.youtube.com/watch?v=BER3EhUIyz0) [Anthropic](https://www.youtube-nocookie.com/channel/UCrDwWp7EBBv4NwvScIpBDOA)

Anthropic627K subscribers

The memory tool operates entirely client-side through tool calls. Developers manage the storage backend, giving them complete control over where the data is stored and how it’s persisted.

Claude Sonnet 4.5 enhances both capabilities with built-in context awareness—tracking available tokens throughout conversations to manage context more effectively.

Together, these updates create a system that improves agent performance:

- Enable longer conversations by automatically removing stale tool results from context
- Boost accuracy by saving critical information to memory—and bring that learning across successive agentic sessions

## Building long-running agents

Claude Sonnet 4.5 is the best model in the world for building agents. These features unlock new possibilities for long-running agents—processing entire codebases, analyzing hundreds of documents, or maintaining extensive tool interaction histories. Context management builds on this foundation, ensuring agents can leverage this expanded capacity efficiently while still handling workflows that extend beyond any fixed limit. Use cases include:

- **Coding:** Context editing clears old file reads and test results while memory preserves debugging insights and architectural decisions, enabling agents to work on large codebases without losing progress.
- **Research:** Memory stores key findings while context editing removes old search results, building knowledge bases that improve performance over time.
- **Data processing:** Agents store intermediate results in memory while context editing clears raw data, handling workflows that would otherwise exceed token limits.

## Performance improvements with context management

On an internal evaluation set for agentic search, we tested how context management improves agent performance on complex, multi-step tasks. The results demonstrate significant gains: combining the memory tool with context editing improved performance by 39% over baseline. Context editing alone delivered a 29% improvement.

In a 100-turn web search evaluation, context editing enabled agents to complete workflows that would otherwise fail due to context exhaustion—while reducing token consumption by 84%.

## Getting started

These capabilities are available today in public beta on the Claude Developer Platform, natively and in Amazon Bedrock and Google Cloud’s Vertex AI. Explore the documentation for [context editing](https://docs.claude.com/en/docs/build-with-claude/context-editing?=) and the [memory tool](https://docs.claude.com/en/docs/agents-and-tools/tool-use/memory-tool?=), or visit our [cookbook](https://platform.claude.com/cookbook/tool-use-memory-cookbook?=) to learn more.

_Anthropic is not affiliated with, endorsed by, or sponsored by CATAN GmbH or CATAN Studio. The CATAN trademark and game are the property of CATAN GmbH._

No items found.

[Prev](https://claude.com/blog/context-management?=#) Prev

0/5

[Next](https://claude.com/blog/context-management?=#) Next

eBook





FAQ

No items found.

## Related posts

Explore more product news and best practices for teams building with Claude.



May 19, 2026

### New in Claude Managed Agents: self-hosted sandboxes and MCP tunnels

Product announcements

[New in Claude Managed Agents: self-hosted sandboxes and MCP tunnels](https://claude.com/blog/context-management?=#) New in Claude Managed Agents: self-hosted sandboxes and MCP tunnels

[New in Claude Managed Agents: self-hosted sandboxes and MCP tunnels](https://claude.com/blog/claude-managed-agents-updates?=) New in Claude Managed Agents: self-hosted sandboxes and MCP tunnels



May 12, 2026

### Code w/ Claude SF 2026 recap: Building on the AI exponential

Product announcements

[Code w/ Claude SF 2026 recap: Building on the AI exponential](https://claude.com/blog/context-management?=#) Code w/ Claude SF 2026 recap: Building on the AI exponential

[Code w/ Claude SF 2026 recap: Building on the AI exponential](https://claude.com/blog/code-w-claude-sf-2026-sf?=) Code w/ Claude SF 2026 recap: Building on the AI exponential



May 12, 2026

### Claude for the legal industry

Product announcements

[Claude for the legal industry](https://claude.com/blog/context-management?=#) Claude for the legal industry

[Claude for the legal industry](https://claude.com/blog/claude-for-the-legal-industry?=) Claude for the legal industry



May 11, 2026

### Introducing the Claude Platform on AWS

Product announcements

[Introducing the Claude Platform on AWS](https://claude.com/blog/context-management?=#) Introducing the Claude Platform on AWS

[Introducing the Claude Platform on AWS](https://claude.com/blog/claude-platform-on-aws?=) Introducing the Claude Platform on AWS

## Transform how your organization operates with Claude

See pricing

[See pricing](https://claude.com/pricing?=#api) See pricing

Contact sales

[Contact sales](https://claude.com/contact-sales?=) Contact sales

Get the developer newsletter

Product updates, how-tos, community spotlights, and more. Delivered monthly to your inbox.

[Subscribe](https://claude.com/blog/context-management?=#) Subscribe

Please provide your email address if you'd like to receive our monthly developer newsletter. You can unsubscribe at any time.

Thank you! You’re subscribed.

Sorry, there was a problem with your submission, please try again later.

[Homepage](https://claude.com/?=) Homepage

[Next](https://claude.com/blog/context-management?=#) Next

Thank you! Your submission has been received!

Oops! Something went wrong while submitting the form.

Write

[Button Text](https://claude.com/blog/context-management?=#) Button Text

Learn

[Button Text](https://claude.com/blog/context-management?=#) Button Text

Code

[Button Text](https://claude.com/blog/context-management?=#) Button Text

Write

- Help me develop a unique voice for an audience











Hi Claude! Could you help me develop a unique voice for an audience? If you need more information from me, ask me 1-2 key questions right away. If you think I should upload any documents that would help you do a better job, let me know. You can use the tools you have access to— like Google Drive, web search, etc.—if they’ll help you better accomplish this task. Do not use analysis tool. Please keep your responses friendly, brief and conversational.



Please execute the task as soon as you can—an artifact would be great if it makes sense. If using an artifact, consider what kind of artifact (interactive, visual, checklist, etc.) might be most helpful for this specific task. Thanks for your help!

- Improve my writing style











Hi Claude! Could you improve my writing style? If you need more information from me, ask me 1-2 key questions right away. If you think I should upload any documents that would help you do a better job, let me know. You can use the tools you have access to— like Google Drive, web search, etc.—if they’ll help you better accomplish this task. Do not use analysis tool. Please keep your responses friendly, brief and conversational.



Please execute the task as soon as you can—an artifact would be great if it makes sense. If using an artifact, consider what kind of artifact (interactive, visual, checklist, etc.) might be most helpful for this specific task. Thanks for your help!

- Brainstorm creative ideas











Hi Claude! Could you brainstorm creative ideas? If you need more information from me, ask me 1-2 key questions right away. If you think I should upload any documents that would help you do a better job, let me know. You can use the tools you have access to— like Google Drive, web search, etc.—if they’ll help you better accomplish this task. Do not use analysis tool. Please keep your responses friendly, brief and conversational.



Please execute the task as soon as you can—an artifact would be great if it makes sense. If using an artifact, consider what kind of artifact (interactive, visual, checklist, etc.) might be most helpful for this specific task. Thanks for your help!


Learn

- Explain a complex topic simply











Hi Claude! Could you explain a complex topic simply? If you need more information from me, ask me 1-2 key questions right away. If you think I should upload any documents that would help you do a better job, let me know. You can use the tools you have access to— like Google Drive, web search, etc.—if they’ll help you better accomplish this task. Do not use analysis tool. Please keep your responses friendly, brief and conversational.



Please execute the task as soon as you can—an artifact would be great if it makes sense. If using an artifact, consider what kind of artifact (interactive, visual, checklist, etc.) might be most helpful for this specific task. Thanks for your help!

- Help me make sense of these ideas











Hi Claude! Could you help me make sense of these ideas? If you need more information from me, ask me 1-2 key questions right away. If you think I should upload any documents that would help you do a better job, let me know. You can use the tools you have access to— like Google Drive, web search, etc.—if they’ll help you better accomplish this task. Do not use analysis tool. Please keep your responses friendly, brief and conversational.



Please execute the task as soon as you can—an artifact would be great if it makes sense. If using an artifact, consider what kind of artifact (interactive, visual, checklist, etc.) might be most helpful for this specific task. Thanks for your help!

- Prepare for an exam or interview











Hi Claude! Could you prepare for an exam or interview? If you need more information from me, ask me 1-2 key questions right away. If you think I should upload any documents that would help you do a better job, let me know. You can use the tools you have access to— like Google Drive, web search, etc.—if they’ll help you better accomplish this task. Do not use analysis tool. Please keep your responses friendly, brief and conversational.



Please execute the task as soon as you can—an artifact would be great if it makes sense. If using an artifact, consider what kind of artifact (interactive, visual, checklist, etc.) might be most helpful for this specific task. Thanks for your help!


Code

- Explain a programming concept











Hi Claude! Could you explain a programming concept? If you need more information from me, ask me 1-2 key questions right away. If you think I should upload any documents that would help you do a better job, let me know. You can use the tools you have access to— like Google Drive, web search, etc.—if they’ll help you better accomplish this task. Do not use analysis tool. Please keep your responses friendly, brief and conversational.



Please execute the task as soon as you can—an artifact would be great if it makes sense. If using an artifact, consider what kind of artifact (interactive, visual, checklist, etc.) might be most helpful for this specific task. Thanks for your help!

- Look over my code and give me tips











Hi Claude! Could you look over my code and give me tips? If you need more information from me, ask me 1-2 key questions right away. If you think I should upload any documents that would help you do a better job, let me know. You can use the tools you have access to— like Google Drive, web search, etc.—if they’ll help you better accomplish this task. Do not use analysis tool. Please keep your responses friendly, brief and conversational.



Please execute the task as soon as you can—an artifact would be great if it makes sense. If using an artifact, consider what kind of artifact (interactive, visual, checklist, etc.) might be most helpful for this specific task. Thanks for your help!

- Vibe code with me











Hi Claude! Could you vibe code with me? If you need more information from me, ask me 1-2 key questions right away. If you think I should upload any documents that would help you do a better job, let me know. You can use the tools you have access to— like Google Drive, web search, etc.—if they’ll help you better accomplish this task. Do not use analysis tool. Please keep your responses friendly, brief and conversational.



Please execute the task as soon as you can—an artifact would be great if it makes sense. If using an artifact, consider what kind of artifact (interactive, visual, checklist, etc.) might be most helpful for this specific task. Thanks for your help!


More

- Write case studies











This is another test

- Write grant proposals











Hi Claude! Could you write grant proposals? If you need more information from me, ask me 1-2 key questions right away. If you think I should upload any documents that would help you do a better job, let me know. You can use the tools you have access to — like Google Drive, web search, etc. — if they’ll help you better accomplish this task. Do not use analysis tool. Please keep your responses friendly, brief and conversational.



Please execute the task as soon as you can - an artifact would be great if it makes sense. If using an artifact, consider what kind of artifact (interactive, visual, checklist, etc.) might be most helpful for this specific task. Thanks for your help!

- Write video scripts











this is a test


[Anthropic](https://www.anthropic.com/) Anthropic

© 2026 Anthropic PBC

Products

- Claude

[Claude](https://claude.com/product/overview?=) Claude

- Claude Code

[Claude Code](https://claude.com/product/claude-code?=) Claude Code

- Claude Code for Enterprise

[Claude Code for Enterprise](https://claude.com/product/claude-code/enterprise?=) Claude Code for Enterprise

- Claude Cowork

[Claude Cowork](https://claude.com/product/cowork?=) Claude Cowork

- Claude Security

[Claude Security](https://claude.com/product/claude-security?=) Claude Security

- Pro plan

[Pro plan](https://claude.com/pricing/pro?=) Pro plan

- Max plan

[Max plan](https://claude.com/pricing/max?=) Max plan

- Team plan

[Team plan](https://claude.com/pricing/team?=) Team plan

- Enterprise plan

[Enterprise plan](https://claude.com/pricing/enterprise?=) Enterprise plan

- Download app

[Download app](https://claude.com/download?=) Download app

- Pricing

[Pricing](https://claude.com/pricing?=) Pricing

- Log in

[Log in](https://claude.ai/login) Log in


Features

- Claude for Chrome

[Claude for Chrome](https://claude.com/claude-for-chrome?=) Claude for Chrome

- Claude for Slack

[Claude for Slack](https://claude.com/claude-for-slack?=) Claude for Slack

- Claude for Microsoft 365

[Claude for Microsoft 365](https://claude.com/claude-for-microsoft-365?=) Claude for Microsoft 365

- Skills

[Skills](https://claude.com/skills?=) Skills


Models

- Mythos Preview

[Mythos Preview](https://www.anthropic.com/glasswing) Mythos Preview

- Opus

[Opus](https://www.anthropic.com/claude/opus) Opus

- Sonnet

[Sonnet](https://www.anthropic.com/claude/sonnet) Sonnet

- Haiku

[Haiku](https://www.anthropic.com/claude/haiku) Haiku


Solutions

- AI agents

[AI agents](https://claude.com/solutions/agents?=) AI agents

- Code modernization

[Code modernization](https://claude.com/solutions/code-modernization?=) Code modernization

- Coding

[Coding](https://claude.com/solutions/coding?=) Coding

- Customer support

[Customer support](https://claude.com/solutions/customer-support?=) Customer support

- Education

[Education](https://claude.com/solutions/education?=) Education

- Financial services

[Financial services](https://claude.com/solutions/financial-services?=) Financial services

- Government

[Government](https://claude.com/solutions/government?=) Government

- Healthcare

[Healthcare](https://claude.com/solutions/healthcare?=) Healthcare

- Legal

[Legal](https://claude.com/solutions/legal?=) Legal

- Life sciences

[Life sciences](https://claude.com/solutions/life-sciences?=) Life sciences

- Nonprofits

[Nonprofits](https://claude.com/solutions/nonprofits?=) Nonprofits

- Security

[Security](https://claude.com/solutions/security?=) Security

- Small business

[Small business](https://claude.com/solutions/small-business?=) Small business


Claude Platform

- Overview

[Overview](https://claude.com/platform/api?=) Overview

- Developer docs

[Developer docs](https://platform.claude.com/docs?=) Developer docs

- Pricing

[Pricing](https://claude.com/pricing?=#api) Pricing

- Marketplace

[Marketplace](https://claude.com/platform/marketplace?=) Marketplace

- Claude on AWS

[Claude on AWS](https://claude.com/partners/claude-on-aws?=) Claude on AWS

- Google Cloud’s Vertex AI

[Google Cloud’s Vertex AI](https://claude.com/partners/google-cloud-vertex-ai?=) Google Cloud’s Vertex AI

- Microsoft Foundry

[Microsoft Foundry](https://claude.com/partners/microsoft-foundry?=) Microsoft Foundry

- Regional compliance

[Regional compliance](https://claude.com/regional-compliance?=) Regional compliance

- Console login

[Console login](https://platform.claude.com/?=) Console login


Resources

- Blog

[Blog](https://claude.com/blog?=) Blog

- Claude partner network

[Claude partner network](https://claude.com/partners?=) Claude partner network

- Community

[Community](https://claude.com/community?=) Community

- Connectors

[Connectors](https://claude.com/connectors?=) Connectors

- Courses

[Courses](https://www.anthropic.com/learn) Courses

- Customer stories

[Customer stories](https://claude.com/customers?=) Customer stories

- Engineering at Anthropic

[Engineering at Anthropic](https://www.anthropic.com/engineering) Engineering at Anthropic

- Events

[Events](https://www.anthropic.com/events) Events

- Plugins

[Plugins](https://claude.com/plugins?=) Plugins

- Powered by Claude

[Powered by Claude](https://claude.com/partners/powered-by-claude?=) Powered by Claude

- Service partners

[Service partners](https://claude.com/partners/services?=) Service partners

- Startups program

[Startups program](https://claude.com/programs/startups?=) Startups program

- Tutorials

[Tutorials](https://claude.com/resources/tutorials?=) Tutorials

- Use cases

[Use cases](https://claude.com/resources/use-cases?=) Use cases


Company

- Anthropic

[Anthropic](https://www.anthropic.com/) Anthropic

- Careers

[Careers](https://www.anthropic.com/careers) Careers

- Economic Futures

[Economic Futures](https://www.anthropic.com/economic-futures) Economic Futures

- Research

[Research](https://www.anthropic.com/research) Research

- News

[News](https://www.anthropic.com/news) News

- Responsible Scaling Policy

[Responsible Scaling Policy](https://www.anthropic.com/news/announcing-our-updated-responsible-scaling-policy) Responsible Scaling Policy

- Security and compliance

[Security and compliance](https://trust.anthropic.com/) Security and compliance

- Transparency

[Transparency](https://anthropic.com/transparency) Transparency


Help and security

- Availability

[Availability](https://www.anthropic.com/supported-countries) Availability

- Status

[Status](https://status.anthropic.com/) Status

- Support center

[Support center](https://support.claude.com/en/?=) Support center


Terms and policies

- Privacy choices











### Cookie settings




We use cookies to deliver and improve our services, analyze site usage, and if you agree, to customize or personalize your experience and market our services to you. You can read our Cookie Policy [here](https://www.anthropic.com/legal/cookies).





Customize cookie settings
Reject all cookies
Accept all cookies









###### Necessary



Enables security and basic functionality.





Required









###### Analytics



Enables tracking of site performance.





Off









###### Marketing



Enables ads personalization and tracking.





Off




Save preferences


- Privacy policy

[Privacy policy](https://www.anthropic.com/legal/privacy) Privacy policy

- Responsible disclosure policy

[Responsible disclosure policy](https://www.anthropic.com/responsible-disclosure-policy) Responsible disclosure policy

- Terms of service: Commercial

[Terms of service: Commercial](https://www.anthropic.com/legal/commercial-terms) Terms of service: Commercial

- Terms of service: Consumer

[Terms of service: Consumer](https://www.anthropic.com/legal/consumer-terms) Terms of service: Consumer

- Usage policy

[Usage policy](https://www.anthropic.com/legal/aup) Usage policy


[x.com](https://x.com/claudeai) x.com

[LinkedIn](https://www.linkedin.com/showcase/claude/) LinkedIn

[YouTube](https://www.youtube.com/@anthropic-ai) YouTube

[Instagram](https://www.instagram.com/claudeai) Instagram

English (US)

Claude Platform

Agents

Business

×