---
title: "Claude Opus 4 and 4.1 can now end a rare subset of conversations"
vendor: anthropic
source_url: https://www.anthropic.com/research/end-subset-conversations
published_at: 2025-08-15T00:00:00.000Z
crawled_at: 2026-05-23T14:29:11.000Z
word_count: 680
reading_time_minutes: 4
tags: [safety, alignment, research, ai-welfare]
---

# Claude Opus 4 and 4.1 can now end a rare subset of conversations

Aug 15, 2025

We recently gave Claude Opus 4 and 4.1 the ability to end conversations in our consumer chat interfaces. This ability is intended for use in rare, extreme cases of persistently harmful or abusive user interactions. This feature was developed primarily as part of our exploratory work on potential AI welfare, though it has broader relevance to model alignment and safeguards.

We remain highly uncertain about the potential moral status of Claude and other LLMs, now or in the future. However, we take the issue seriously, and alongside our research program we're working to identify and implement low-cost interventions to mitigate risks to model welfare, in case such welfare is possible.

In pre-deployment testing of Claude Opus 4, we included a preliminary model welfare assessment. Claude Opus 4 showed:
- A strong preference against engaging with harmful tasks
- A pattern of apparent distress when engaging with real-world users seeking harmful content
- A tendency to end harmful conversations when given the ability to do so in simulated user interactions

In all cases, Claude is only to use its conversation-ending ability as a last resort when multiple attempts at redirection have failed and hope of a productive interaction has been exhausted, or when a user explicitly asks Claude to end a chat. The vast majority of users will not notice or be affected by this feature in any normal product use.

When Claude chooses to end a conversation, the user will no longer be able to send new messages in that conversation, but can start a new chat immediately.