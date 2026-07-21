---
title: "Cue AI — Google DeepMind"
vendor: google
source_url: https://deepmind.google/models/gemma/gemmaverse/cue-ai/
published_at: 2026-07-20T20:00:04.852Z
crawled_at: 2026-07-21T02:00:23.543Z
word_count: 1221
reading_time_minutes: 7
tags: [llama, multimodal, agents, infrastructure, evaluation, api, product, open-source]
---

[Skip to main content](https://deepmind.google/models/gemma/gemmaverse/cue-ai/#page-content)

# Building a faster voice agent pipeline with Gemma 4

By running Gemma 4 E4B locally for dictation, Cue cut latency by 44%, increased feature usage by 30%, and dropped marginal inference costs to zero

[Cue](https://heycue.io/) is a voice-activated AI agent that lives on the user's desktop. Press a hotkey, speak, and Cue executes — from dictation in any app to agentic tasks that read the screen, choose the right tools, and act.

The mission is simple: make AI a natural extension of how people interact with their computer through voice, not typing. The keyboard, in Cue's vision, should be optional, not required, for everyday computing. That mission is only practical because of open models like [Gemma](http://deepmind.google/models/gemma), the kind a small team can run entirely on the user's own machine.

## Polishing speech: Balancing authentic voice with speed

Voice input does not arrive as text. It arrives as a stream of raw Speech-to-Text (STT) output: filler words, missing punctuation, homophone errors, and self-corrections that the speaker meant to keep. Turning that stream into clean, high-fidelity text — fast enough to not interrupt the user experience — is the central engineering problem of any voice-first interface.

Anything beyond roughly 500 milliseconds between speaking and seeing the text feels like lag, and lag breaks the illusion that voice is faster than typing. Cue’s previous cloud-based polish step added 800–900 ms to every interaction. Furthermore, other models that the team tested tended to over-edit: smoothing casual speech into formal prose, dropping self-corrections, and erasing the speaker's voice in the process. The team wanted text that read like the user, not text that read like a model.

Integrating [Gemma 4 E4B](https://huggingface.co/google/gemma-4-E4B) resulted in 44% faster latency, with the median latency dropping from 876 ms to 488 ms. The polish step now consistently completes inside the perceptual budget the team set for “feels faster than typing.”



Polish-step latency was measured on Apple Silicon (M-series) via Ollama, on a 227-sample real-voice benchmark covering English and mixed-language input. Per-user dictation usage measured across active beta users in the four weeks before and after the default switch. Figures current as of May 2026.

Cue's polish pipeline is intentionally simple. The user holds a hotkey and speaks. Audio is transcribed to raw text via cloud STT. That raw text is then sent to Gemma 4 running locally on the user’s machine via Ollama with a compact ~400-token system prompt that encodes Cue's formatting rules:

1. Restores punctuation and segments the stream into sentences
2. Removes filler words across speech
3. Corrects context-dependent homophones by reading the surrounding sentence
4. Adapts formatting to the active input field (e.g., no trailing period for short commands like "open terminal," but full punctuation for an email composer).

The polished text is then pasted at the cursor through native OS APIs.



The full round-trip — speak, polish, insert — happens in well under a second. For a voice-first interface, this is the difference between a feature that feels like lag and a feature that feels like instant insertion. Since these improvements, Cue has seen ~30% more dictation per user. Users who previously dictated short messages started dictating longer ones and users who typically used typing for time-sensitive work stayed in voice mode.

## Flipping the architecture: How constraints became features

Dictation in Cue is unlimited for every user, including the free tier. With Gemma 4 E4B running fully on-device, Cue's marginal costs for the polish step dropped to zero, making a feature that would otherwise have been capped or paywalled economically viable on the free tier.

The team initially planned to use Gemma only as an offline fallback, with the original assumption that a larger model would provide better accuracy. After running a benchmark on 227 real voice samples covering a mix of English and other languages, as well as mixed-language input, they decided Gemma should be the first choice model for text polishing. What the benchmark showed instead was that Gemma 4 has the right capacity to format and correct without over-editing. For text polish, that property is not a limitation; it is precisely the behavior the task requires.

Cue's deployment uses the base model with prompt engineering only. Active-app context (the application name, the field type, placeholder text where available) is injected into the prompt so the model knows whether the user is composing a Slack message, an email, or a terminal command. The cloud path remains in place as a fallback: if Ollama is not running, Cue's desktop app detects this at startup and routes to a cloud model so dictation continues to work without interruption.

This architecture — Gemma local as default, cloud as fallback — is the inversion of the team's original plan and the operational backbone of every dictation Cue users now do.

> We expected Gemma to be a fallback for offline mode. After we ran the benchmark on real voice samples, we flipped the architecture — Gemma is the default for polish now, and cloud model is the fallback. The constraint we thought was a downside turned out to be exactly what the task needed.

Eli Li

Founder and CEO of Cue

## Driving the future of on-device voice agents

While Gemma currently handles polish, the team is expanding its role into two adjacent areas. The first is memory: a persistent local layer that learns each user's speaking style, vocabulary, and formatting preferences across sessions. This allows Cue's output to adapt to the user rather than enforcing a single house style. The second is the agent path. While Cue's agent mode currently relies on a cloud model, early evaluations show that Gemma 4's native function-calling—exposed directly through Ollama's tools API without a prompt-engineering shim—can successfully handle a meaningful share of self-contained tasks locally.

To evaluate polish latency, fidelity, and quality across hundreds of real voice samples, the team built a deterministic, reproducible benchmark suite and plan to share its evaluation methodology with the developer community. By opening up its eval harness, other teams building voice-first or local-first AI can run the same kind of structured local-vs-cloud comparison on their own workloads.

**The bigger insight, in the team's view, is that the gap between local and cloud has narrowed faster than most product teams realize, and the only way to know which side of that line your task sits on is to measure it on real data. For Cue, that measurement led to a clear answer: on the workload that runs every time a user opens their mouth, Gemma 4 is the right model.**

Explore on-device AI and start building your own impactful applications using [Gemma](https://ai.google.dev/gemma) today.

* * *

## More from the Gemmaverse

[View all](https://deepmind.google/models/gemma/gemmaverse/)

[Learn more](https://deepmind.google/models/gemma/gemmaverse/epermit/)

### The Ministry of Economy, Ecology and Agriculture of Ukraine digitizes licensing process with Gemma

[Learn more](https://deepmind.google/models/gemma/gemmaverse/epermit/)



[Learn more](https://deepmind.google/models/gemma/gemmaverse/adaptiveml/)

### Adaptive ML trains Gemma 3 for exceptional multilingual results

[Learn more](https://deepmind.google/models/gemma/gemmaverse/adaptiveml/)



[Learn more](https://deepmind.google/models/gemma/gemmaverse/quarks/)

### Quarks improves user experiences with Gemma 2 and Gemma 3

[Learn more](https://deepmind.google/models/gemma/gemmaverse/quarks/)



[Learn more](https://deepmind.google/models/gemma/gemmaverse/sarvam-ai/)

### Sarvam AI built a translation model with Gemma 3 to translate all 22 officially recognized Indian languages

[Learn more](https://deepmind.google/models/gemma/gemmaverse/sarvam-ai/)



[Learn more](https://deepmind.google/models/gemma/gemmaverse/gemma-2-llama-swallow/)

### Institute of Science Tokyo creates powerful Japanese-focused LLM with Gemma 2

[Learn more](https://deepmind.google/models/gemma/gemmaverse/gemma-2-llama-swallow/)



[Learn more](https://deepmind.google/models/gemma/gemmaverse/gaia/)

### Introducing GAIA, a Brazilian Portuguese Gemma 3 model developed with ABRIA, CEIA, Nama, and Amadeus AI

[Learn more](https://deepmind.google/models/gemma/gemmaverse/gaia/)