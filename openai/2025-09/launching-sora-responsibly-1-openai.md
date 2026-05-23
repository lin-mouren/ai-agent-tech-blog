---
title: "Launching Sora responsibly"
vendor: openai
source_url: https://openai.com/index/launching-sora-responsibly/
published_at: 2025-09-30T00:00:00.000Z
crawled_at: 2026-05-23T14:36:57.000Z
word_count: 1417
reading_time_minutes: 8
tags: [sora, safety, video-generation, ai-safety, multimodal]
---

Sora 2 and the Sora app combine cutting-edge video generation with a new way to create together, and we've made sure safety is built in from the very start. Our approach is anchored in concrete protections:

- **Distinguishing AI content.** Every video generated with Sora includes both visible and invisible provenance signals. At launch, all outputs carry a visible watermark. All Sora videos also embed C2PA metadata—an industry-standard signature—and we maintain internal reverse-image and audio search tools that can trace videos back to Sora with high accuracy, building on successful systems from ChatGPT image generation and Sora 1.

- **Consent-based likeness using characters.** Our goal is to place you in control of your likeness end-to-end with Sora characters. We have guardrails intended to ensure that your audio and image likeness captured in characters are used with your consent. Only you decide who can use your characters, and you can revoke access at any time. We also take measures to block depictions of public figures (except those using the characters feature, of course). Videos that include your characters—including drafts created by other users—are always visible to you. This lets you easily review and delete (and, if needed, report) any videos featuring your character. We also apply extra safety guardrails to any video with a character, and you can even set preferences for how your character behaves—for example, requesting that it always wears a fedora.

- **Safeguards for teens.** Sora includes stronger protections for younger users, including limitations on mature output. The feed is designed to be appropriate for teens, teen profiles are not recommended to adults, and adults cannot initiate messages with teens. New parental controls in ChatGPT let parents manage whether teens can send and receive DMs, as well as select a non-personalized feed in the Sora app. And by default, teens also have limits on how much they can continuously scroll in Sora.

- **Filtering harmful content.** Sora uses layered defenses to keep the feed safe while leaving room for creativity. At creation, guardrails seek to block unsafe content before it's made—including sexual material, terrorist propaganda, and self-harm promotion—by checking both prompts and outputs across multiple video frames and audio transcripts. We've red teamed to explore novel risks, and we've tightened policies relative to image generation given Sora's greater realism and the addition of motion and audio. Beyond generation, automated systems scan all feed content against our Global Usage Policies and filter out unsafe or age-inappropriate material. These systems are continuously updated as we learn about new risks and are complemented by human review focused on the highest-impact harms.

- **Audio safeguards.** Adding audio to Sora raises the bar for safety, and while perfect protections are difficult, we continue to invest seriously in this area. Sora automatically scans transcripts of generated speech for potential policy violations, and also blocks attempts to generate music that imitates living artists or existing works. Our systems are designed to detect and stop such prompts, and we honor takedown requests from creators who believe a Sora output infringes on their work.

- **User control and recourse.** You choose when and how to share your videos, and you can remove your published content at any time. Videos will only be shared to the feed when you choose to do so. Every video, profile, and comment can be reported for abuse, with clear recourse when policies are violated. You can also choose to block accounts at any time, which will prevent others from seeing your profile or contacting you via direct message.

The Sora team