---
title: "Gemini API tooling updates: context circulation, tool combos and Maps grounding"
vendor: google
source_url: https://blog.google/innovation-and-ai/technology/developers-tools/gemini-api-tooling-updates/
published_at: 2026-03-17T16:00:00.000Z
crawled_at: 2026-05-22T06:01:55.182Z
word_count: 1009
reading_time_minutes: 6
tags: [gemini, reasoning, agents, infrastructure, api, product]
---

# Gemini API tooling updates: context circulation, tool combos and Maps grounding for Gemini 3

Mar 17, 2026

·

2 min read

Share

[x.com](https://twitter.com/intent/tweet?text=Gemini%20API%20tooling%20updates%3A%20context%20circulation%2C%20tool%20combos%20and%20Maps%20grounding%20for%20Gemini%203%20%40google&url=https://blog.google/innovation-and-ai/technology/developers-tools/gemini-api-tooling-updates/) [Facebook](https://www.facebook.com/sharer/sharer.php?caption=Gemini%20API%20tooling%20updates%3A%20context%20circulation%2C%20tool%20combos%20and%20Maps%20grounding%20for%20Gemini%203&u=https://blog.google/innovation-and-ai/technology/developers-tools/gemini-api-tooling-updates/) [LinkedIn](https://www.linkedin.com/shareArticle?mini=true&url=https://blog.google/innovation-and-ai/technology/developers-tools/gemini-api-tooling-updates/&title=Gemini%20API%20tooling%20updates%3A%20context%20circulation%2C%20tool%20combos%20and%20Maps%20grounding%20for%20Gemini%203) [Mail](mailto:?subject=Gemini%20API%20tooling%20updates%3A%20context%20circulation%2C%20tool%20combos%20and%20Maps%20grounding%20for%20Gemini%203&body=Check%20out%20this%20article%20on%20the%20Keyword:%0A%0AGemini%20API%20tooling%20updates%3A%20context%20circulation%2C%20tool%20combos%20and%20Maps%20grounding%20for%20Gemini%203%0A%0ADevelopers%20can%20now%20combine%20function%20calling%20with%20built-in%20tools%20such%20as%20Google%20Search%20in%20a%20single%20Gemini%20API%20call%20to%20build%20agentic%20and%20complex%20tool-use%20applications.%0A%0Ahttps://blog.google/innovation-and-ai/technology/developers-tools/gemini-api-tooling-updates/)

Copy link

Developers can now combine function calling with built-in tools such as Google Search in a single Gemini API call to build agentic and complex tool-use applications.


M

Mariano Cocirio

Product Manager, Google DeepMind


![Philipp Schmid](https://storage.googleapis.com/gweb-uniblog-publish-prod/original_images/72.png)

Philipp Schmid

Developer Relations Engineer, Google DeepMind


Share

[x.com](https://twitter.com/intent/tweet?text=Gemini%20API%20tooling%20updates%3A%20context%20circulation%2C%20tool%20combos%20and%20Maps%20grounding%20for%20Gemini%203%20%40google&url=https://blog.google/innovation-and-ai/technology/developers-tools/gemini-api-tooling-updates/) [Facebook](https://www.facebook.com/sharer/sharer.php?caption=Gemini%20API%20tooling%20updates%3A%20context%20circulation%2C%20tool%20combos%20and%20Maps%20grounding%20for%20Gemini%203&u=https://blog.google/innovation-and-ai/technology/developers-tools/gemini-api-tooling-updates/) [LinkedIn](https://www.linkedin.com/shareArticle?mini=true&url=https://blog.google/innovation-and-ai/technology/developers-tools/gemini-api-tooling-updates/&title=Gemini%20API%20tooling%20updates%3A%20context%20circulation%2C%20tool%20combos%20and%20Maps%20grounding%20for%20Gemini%203) [Mail](mailto:?subject=Gemini%20API%20tooling%20updates%3A%20context%20circulation%2C%20tool%20combos%20and%20Maps%20grounding%20for%20Gemini%203&body=Check%20out%20this%20article%20on%20the%20Keyword:%0A%0AGemini%20API%20tooling%20updates%3A%20context%20circulation%2C%20tool%20combos%20and%20Maps%20grounding%20for%20Gemini%203%0A%0ADevelopers%20can%20now%20combine%20function%20calling%20with%20built-in%20tools%20such%20as%20Google%20Search%20in%20a%20single%20Gemini%20API%20call%20to%20build%20agentic%20and%20complex%20tool-use%20applications.%0A%0Ahttps://blog.google/innovation-and-ai/technology/developers-tools/gemini-api-tooling-updates/)

Copy link

![Gemini API header with code snippet showing an example of a multi-tool combination flow with Grounding with Google Search.](https://storage.googleapis.com/gweb-uniblog-publish-prod/images/gemini-API_blog_keyword_header_3.width-200.format-webp.webp)

As agentic workflows scale, orchestration can become a bottleneck. Today, we’re simplifying this by allowing developers to [combine](https://ai.google.dev/gemini-api/docs/tool-combination) built-in tools (such as Google Search and Google Maps) with custom functions in a single request, [circulate context](https://ai.google.dev/gemini-api/docs/tool-combination#how-it-works) across tool calls and turns for more complex reasoning and extend [Grounding with Google Maps](https://ai.google.dev/gemini-api/docs/maps-grounding) to the Gemini 3 model family.

## New tooling capabilities in the API

### Combine built-in and custom tools in the same interaction

Previously, developers had to carefully orchestrate when to use built-in tools (like Google Search) versus when to rely on a custom function declaration. Now, you can [pass both built-in tools and your own custom tools](https://ai.google.dev/gemini-api/docs/tool-combination) in the same request. This allows Gemini to easily pivot between fetching public data via Google Search then calling your backend without separate orchestration steps, reducing end-to-end latency and simplifying agent architectures.

This has been a top request from developers since we introduced built-in tools and we are excited to see how you combine file search, Google Maps, Search, and custom functions together!

### Cross-tool context circulation for built-in tools

In multi-step workflows, models often need to use the output of one tool as the input for another. [Context circulation](https://ai.google.dev/gemini-api/docs/tool-combination#how-it-works) for built-in tools preserves every tool call and its response in the model's context, so follow-up steps can access and reason over that data. For example, Gemini can now use a built-in tool to get real-time weather data and circulate that context to a custom tool that books a venue.

### Tool response IDs

To improve debuggability and ensure precise mapping during asynchronous tool executions, we’ve introduced [unique call identifiers](https://ai.google.dev/gemini-api/docs/tool-combination#critical-fields) (\`id\`) for every tool call. These IDs allow developers to identify specific tool calls requested by the model with the exact client responses, which is especially critical when handling parallel function calling and cross-tool context.

Here’s a code snippet showing an example of a multi-tool combination flow with [Grounding with Google Search](https://ai.google.dev/gemini-api/docs/google-search).

```py
from google import genai

client = genai.Client()

check_inventory = {
    "type": "function",
    "name": "check_inventory",
    "description": "Checks the internal inventory database for a specific product model.",
    "parameters": {
        "type": "object",
        "properties": {
            "product_name": {
                "type": "string",
                "description": "The name or model of the product to check",
            }
        },
        "required": ["product_name"],
    },
}

interaction = client.interactions.create(
    model="gemini-3-flash-preview",
    input=(
        "Search the web for the top 3 trending noise-canceling headphones today, "
        "and then check if we have those specific models in our internal inventory."
    ),
    tools=[\
        {"type": "google_search"}, # Built-in tool\
        check_inventory,           # Custom function\
    ],
)

for output in interaction.outputs:
    if output.type == "function_call":
        print(f"Tool ID: {output.id}")
        print(f"Calling: {output.name} with args: {output.arguments}")
    elif output.type == "text":
        print(output.text)
```

## Expanded built-in tooling support

### Grounding with Google Maps for the Gemini 3 family

Location context is an important building block when building modern agents so today we’re launching support for [Grounding with Google Maps](https://ai.google.dev/gemini-api/docs/maps-grounding) for the Gemini 3 family of models. You can now enable Maps as a tool for your Gemini 3 model of choice to access rich, up-to-date spatial data, local business information, commute times, and place details to provide more accurate and location-aware responses.

```py
from google import genai

client = genai.Client()

interaction = client.interactions.create(
    model="gemini-3-flash-preview",
    input=(
        "Find three highly-rated coffee shops open right now "
        "within walking distance of Alexanderplatz in Berlin."
    ),
    tools=[{"type": "google_maps"}],
)
```

While these features are also supported in the generateContent API, we recommend using the new [Interactions API](https://ai.google.dev/gemini-api/docs/interactions?ua=chat) for these workflows to take advantage of its server-side state management and unified reasoning traces.

Whether you're combining Grounding with Google Maps with your internal inventory APIs, or letting the model naturally circulate context between custom tools, you can turn complex agentic workflows into reality easily. [Start building](http://ai.google.dev/gemini-api) today.

POSTED IN:

### Related stories

[![](https://storage.googleapis.com/gweb-uniblog-publish-prod/images/100_things_Social.width-300.format-webp.webp)\\
\\
AI **100 things we announced at I/O 2026**\\
\\
By\\
\\
\\
\\
Keyword Team\\
\\
\\
May 20, 2026](https://blog.google/innovation-and-ai/technology/ai/google-io-2026-all-our-announcements/)

[![](https://storage.googleapis.com/gweb-uniblog-publish-prod/images/FINAL_SOCIAL_HERO_laWfMt0.width-300.format-webp.webp)\\
\\
AI Products **Making it easier to understand how content was created and edited**\\
\\
By\\
\\
\\
\\
Laurie Richardson\\
\\
\\
\\
&\\
\\
\\
Pushmeet Kohli\\
\\
\\
May 19, 2026](https://blog.google/innovation-and-ai/products/identifying-ai-generated-media-online/)

[![](https://storage.googleapis.com/gweb-uniblog-publish-prod/images/Introducing_Managed_Agents_in_the.width-300.format-webp.webp)\\
\\
Developer tools **Introducing Managed Agents in the Gemini API**\\
\\
By\\
\\
\\
\\
Ali Çevik\\
\\
\\
\\
&\\
\\
\\
Philipp Schmid\\
\\
\\
May 19, 2026](https://blog.google/innovation-and-ai/technology/developers-tools/managed-agents-gemini-api/)

[![](https://storage.googleapis.com/gweb-uniblog-publish-prod/images/science__keyword__blog-header.width-300.format-webp.webp)\\
\\
Google Research **Gemini for Science: AI experiments and tools for a new era of discovery**\\
\\
By\\
\\
\\
\\
Pushmeet Kohli\\
\\
\\
\\
&\\
\\
\\
Yossi Matias](https://blog.google/innovation-and-ai/technology/research/gemini-for-science-io-2026/)

[![](https://storage.googleapis.com/gweb-uniblog-publish-prod/images/Vibe_Dark_Mode.width-300.format-webp.webp)\\
\\
Developer tools **Bring any idea to life: Google AI Studio at I/O 2026**\\
\\
By\\
\\
\\
\\
Ammaar Reshi\\
\\
\\
\\
&\\
\\
\\
Mike Taylor-Cai\\
\\
\\
May 19, 2026](https://blog.google/innovation-and-ai/technology/developers-tools/google-ai-studio-io-2026/)

[![](https://storage.googleapis.com/gweb-uniblog-publish-prod/images/I_O_26_Header_1_AYohnR4.width-300.format-webp.webp)\\
\\
Google One **Everything new in our Google AI subscriptions, fresh from I/O 2026**\\
\\
By\\
\\
\\
\\
Shimrit Ben-Yair\\
\\
\\
May 19, 2026](https://blog.google/products-and-platforms/products/google-one/google-ai-subscriptions/)

.

Jump to position 1
Jump to position 2
Jump to position 3
Jump to position 4
Jump to position 5
Jump to position 6

![](https://blog.google/static/blogv2/images/newsletter_toast.svg?version=pr20260507-1819)

Let’s stay in touch. Get the latest news from Google in your inbox.

[Subscribe](https://blog.google/newsletter-subscribe/) No thanks

Survey

Help us improve The Keyword with a one-question survey

YesNo

This survey is anonymous. All responses will be aggregated and used only for analysis to improve our services.

Did this article provide the level of detail you were looking for?

Yes, I got what I neededNo, I wanted more technical depthNo, I wanted a simpler overviewI was looking for something else entirely

✅

Thank you!