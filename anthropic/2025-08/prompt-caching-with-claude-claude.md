---
title: "Prompt caching with Claude | Claude"
vendor: anthropic
source_url: https://www.anthropic.com/news/prompt-caching?s=09
published_at: 2025-08-14T14:58:10.000Z
crawled_at: 2026-05-23T02:01:32.978Z
word_count: 2924
reading_time_minutes: 15
tags: [agents, infrastructure, api, product, enterprise, coding]
---

[Home page](https://claude.com/?s=09)

Explore here



# Prompt    caching    with    Claude

Claude caches frequently used context between API calls, reducing costs and latency for long prompts.

- Category







[Product announcements](https://claude.com/blog/category/announcements?s=09)

- Product









Claude Platform

- Date



August 14, 2025

- Reading time





5



min

- Share

[Copy link](https://claude.com/blog/prompt-caching?s=09#)

https://claude.com/blog/prompt-caching


**_Update_** _: Prompt caching is Generally Available on the Anthropic API. Prompt caching is also available in preview in Amazon Bedrock and on Google Cloud’s Vertex AI. (December 17, 2024)_ Prompt caching, which enables developers to cache frequently used context between API calls, is now available on the Anthropic API. With prompt caching, customers can provide Claude with more background knowledge and example outputs—all while reducing costs by up to 90% and latency by up to 85% for long prompts. Prompt caching is available today in public beta for Claude 3.5 Sonnet, Claude 3 Opus, and Claude 3 Haiku.

## When to use prompt caching

Prompt caching can be effective in situations where you want to send a large amount of prompt context once and then refer to that information repeatedly in subsequent requests, including:

- **Conversational agents:** Reduce cost and latency for extended conversations, especially those with long instructions or uploaded documents.
- **Coding assistants:** Improve autocomplete and codebase Q&A by keeping a summarized version of the codebase in the prompt.
- **Large document processing:** Incorporate complete long-form material including images in your prompt without increasing response latency.
- **Detailed instruction sets:** Share extensive lists of instructions, procedures, and examples to fine-tune Claude's responses. Developers often include a few examples in their prompt, but with prompt caching you can get even better performance by including dozens of diverse examples of high quality outputs.
- **Agentic search and tool use:** Enhance performance for scenarios involving multiple rounds of tool calls and iterative changes, where each step typically requires a new API call.
- **Talk to books, papers, documentation, podcast transcripts, and other long-form content:** Bring any knowledge base alive by embedding the entire document(s) into the prompt, and letting users ask it questions.


Early customers have seen substantial speed and cost improvements with prompt caching for a variety of use cases—from including a full knowledge base to 100-shot examples to including each turn of a conversation in their prompt.

| **Use case** | **Latency w/o caching (time to first token)** | **Latency w/ caching (time to first token)** | **Cost reduction** |
| --- | --- | --- | --- |
| Chat with a book (100,000 token cached prompt) \[1\] | 11.5s | 2.4s (-79%) | -90% |
| Many-shot prompting (10,000 token prompt) \[1\] | 1.6s | 1.1s (-31%) | -86% |
| Multi-turn conversation (10-turn convo with a long system prompt)<br> \[2\] | ~10s | ~2.5s (-75%) | -53% |

Prompt caching

### How we price cached prompts

Cached prompts are priced based on the number of input tokens you cache and how frequently you use that content. Writing to the cache costs 25% more than our base input token price for any given model, while using cached content is significantly cheaper, costing only 10% of the base input token price.

|     |     |     |     |
| --- | --- | --- | --- |
| **Claude 3.5 Sonnet**<br>- Our most intelligent model to date<br>- 200K context window | **Input**<br>- $3 / MTok | **Prompt caching**<br>- $3.75 / MTok -<br>   Cache write<br>   <br>- $0.30 / MTok - Cache read | **Output**<br>- $15 / MTok |
| **Claude 3 Opus**<br>- Powerful model for complex tasks<br>- 200K context window | **Input**<br>- $15 / MTok | **Prompt caching**<br>- $18.75 / MTok -<br>   Cache write<br>   <br>- $1.50 / MTok - Cache read | **Output**<br>- $75 / MTok |
| **Claude 3 Haiku**<br>- Fastest, most cost-effective model<br>- 200K context window | **Input**<br>- $0.25 / MTok | **Prompt caching**<br>- $0.30 / MTok<br>   -<br>   Cache write<br>   <br>- $0.03 / MTok - Cache read | **Output**<br>- $1.25 / MTok |

Pricing

### Customer spotlight: Notion

[Notion](https://www.notion.so/product/ai) is adding prompt caching to Claude-powered features for its AI assistant, Notion AI. With reduced costs and increased speed, Notion is able to optimize internal operations and create a more elevated and responsive user experience for their customers.

> We're excited to use prompt caching to make Notion AI faster and cheaper, all while maintaining state-of-the-art quality.

— Simon Last, Co-founder at Notion

### Get started

To start using the prompt caching public beta on the Anthropic API, explore our [documentation](https://docs.anthropic.com/en/docs/build-with-claude/prompt-caching) and [pricing page](https://www.anthropic.com/pricing#anthropic-api).

No items found.

[Prev](https://claude.com/blog/prompt-caching?s=09#) Prev

0/5

[Next](https://claude.com/blog/prompt-caching?s=09#) Next

eBook





FAQ

No items found.

## Related posts

Explore more product news and best practices for teams building with Claude.



May 19, 2026

### New in Claude Managed Agents: self-hosted sandboxes and MCP tunnels

Product announcements

[New in Claude Managed Agents: self-hosted sandboxes and MCP tunnels](https://claude.com/blog/prompt-caching?s=09#) New in Claude Managed Agents: self-hosted sandboxes and MCP tunnels

[New in Claude Managed Agents: self-hosted sandboxes and MCP tunnels](https://claude.com/blog/claude-managed-agents-updates?s=09) New in Claude Managed Agents: self-hosted sandboxes and MCP tunnels



May 12, 2026

### Code w/ Claude SF 2026 recap: Building on the AI exponential

Product announcements

[Code w/ Claude SF 2026 recap: Building on the AI exponential](https://claude.com/blog/prompt-caching?s=09#) Code w/ Claude SF 2026 recap: Building on the AI exponential

[Code w/ Claude SF 2026 recap: Building on the AI exponential](https://claude.com/blog/code-w-claude-sf-2026-sf?s=09) Code w/ Claude SF 2026 recap: Building on the AI exponential



May 12, 2026

### Claude for the legal industry

Product announcements

[Claude for the legal industry](https://claude.com/blog/prompt-caching?s=09#) Claude for the legal industry

[Claude for the legal industry](https://claude.com/blog/claude-for-the-legal-industry?s=09) Claude for the legal industry



May 11, 2026

### Introducing the Claude Platform on AWS

Product announcements

[Introducing the Claude Platform on AWS](https://claude.com/blog/prompt-caching?s=09#) Introducing the Claude Platform on AWS

[Introducing the Claude Platform on AWS](https://claude.com/blog/claude-platform-on-aws?s=09) Introducing the Claude Platform on AWS

## Transform how your organization operates with Claude

See pricing

[See pricing](https://claude.com/pricing?s=09#api) See pricing

Contact sales

[Contact sales](https://claude.com/contact-sales?s=09) Contact sales

Get the developer newsletter

Product updates, how-tos, community spotlights, and more. Delivered monthly to your inbox.

[Subscribe](https://claude.com/blog/prompt-caching?s=09#) Subscribe

Please provide your email address if you'd like to receive our monthly developer newsletter. You can unsubscribe at any time.

Thank you! You’re subscribed.

Sorry, there was a problem with your submission, please try again later.

[Homepage](https://claude.com/?s=09) Homepage

[Next](https://claude.com/blog/prompt-caching?s=09#) Next

Thank you! Your submission has been received!

Oops! Something went wrong while submitting the form.

Write

[Button Text](https://claude.com/blog/prompt-caching?s=09#) Button Text

Learn

[Button Text](https://claude.com/blog/prompt-caching?s=09#) Button Text

Code

[Button Text](https://claude.com/blog/prompt-caching?s=09#) Button Text

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

[Claude](https://claude.com/product/overview?s=09) Claude

- Claude Code

[Claude Code](https://claude.com/product/claude-code?s=09) Claude Code

- Claude Code for Enterprise

[Claude Code for Enterprise](https://claude.com/product/claude-code/enterprise?s=09) Claude Code for Enterprise

- Claude Cowork

[Claude Cowork](https://claude.com/product/cowork?s=09) Claude Cowork

- Claude Security

[Claude Security](https://claude.com/product/claude-security?s=09) Claude Security

- Pro plan

[Pro plan](https://claude.com/pricing/pro?s=09) Pro plan

- Max plan

[Max plan](https://claude.com/pricing/max?s=09) Max plan

- Team plan

[Team plan](https://claude.com/pricing/team?s=09) Team plan

- Enterprise plan

[Enterprise plan](https://claude.com/pricing/enterprise?s=09) Enterprise plan

- Download app

[Download app](https://claude.com/download?s=09) Download app

- Pricing

[Pricing](https://claude.com/pricing?s=09) Pricing

- Log in

[Log in](https://claude.ai/login) Log in


Features

- Claude for Chrome

[Claude for Chrome](https://claude.com/claude-for-chrome?s=09) Claude for Chrome

- Claude for Slack

[Claude for Slack](https://claude.com/claude-for-slack?s=09) Claude for Slack

- Claude for Microsoft 365

[Claude for Microsoft 365](https://claude.com/claude-for-microsoft-365?s=09) Claude for Microsoft 365

- Skills

[Skills](https://claude.com/skills?s=09) Skills


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

[AI agents](https://claude.com/solutions/agents?s=09) AI agents

- Code modernization

[Code modernization](https://claude.com/solutions/code-modernization?s=09) Code modernization

- Coding

[Coding](https://claude.com/solutions/coding?s=09) Coding

- Customer support

[Customer support](https://claude.com/solutions/customer-support?s=09) Customer support

- Education

[Education](https://claude.com/solutions/education?s=09) Education

- Financial services

[Financial services](https://claude.com/solutions/financial-services?s=09) Financial services

- Government

[Government](https://claude.com/solutions/government?s=09) Government

- Healthcare

[Healthcare](https://claude.com/solutions/healthcare?s=09) Healthcare

- Legal

[Legal](https://claude.com/solutions/legal?s=09) Legal

- Life sciences

[Life sciences](https://claude.com/solutions/life-sciences?s=09) Life sciences

- Nonprofits

[Nonprofits](https://claude.com/solutions/nonprofits?s=09) Nonprofits

- Security

[Security](https://claude.com/solutions/security?s=09) Security

- Small business

[Small business](https://claude.com/solutions/small-business?s=09) Small business


Claude Platform

- Overview

[Overview](https://claude.com/platform/api?s=09) Overview

- Developer docs

[Developer docs](https://platform.claude.com/docs?s=09) Developer docs

- Pricing

[Pricing](https://claude.com/pricing?s=09#api) Pricing

- Marketplace

[Marketplace](https://claude.com/platform/marketplace?s=09) Marketplace

- Claude on AWS

[Claude on AWS](https://claude.com/partners/claude-on-aws?s=09) Claude on AWS

- Google Cloud’s Vertex AI

[Google Cloud’s Vertex AI](https://claude.com/partners/google-cloud-vertex-ai?s=09) Google Cloud’s Vertex AI

- Microsoft Foundry

[Microsoft Foundry](https://claude.com/partners/microsoft-foundry?s=09) Microsoft Foundry

- Regional compliance

[Regional compliance](https://claude.com/regional-compliance?s=09) Regional compliance

- Console login

[Console login](https://platform.claude.com/?s=09) Console login


Resources

- Blog

[Blog](https://claude.com/blog?s=09) Blog

- Claude partner network

[Claude partner network](https://claude.com/partners?s=09) Claude partner network

- Community

[Community](https://claude.com/community?s=09) Community

- Connectors

[Connectors](https://claude.com/connectors?s=09) Connectors

- Courses

[Courses](https://www.anthropic.com/learn) Courses

- Customer stories

[Customer stories](https://claude.com/customers?s=09) Customer stories

- Engineering at Anthropic

[Engineering at Anthropic](https://www.anthropic.com/engineering) Engineering at Anthropic

- Events

[Events](https://www.anthropic.com/events) Events

- Plugins

[Plugins](https://claude.com/plugins?s=09) Plugins

- Powered by Claude

[Powered by Claude](https://claude.com/partners/powered-by-claude?s=09) Powered by Claude

- Service partners

[Service partners](https://claude.com/partners/services?s=09) Service partners

- Startups program

[Startups program](https://claude.com/programs/startups?s=09) Startups program

- Tutorials

[Tutorials](https://claude.com/resources/tutorials?s=09) Tutorials

- Use cases

[Use cases](https://claude.com/resources/use-cases?s=09) Use cases


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

[Support center](https://support.claude.com/en/?s=09) Support center


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

Coding

×