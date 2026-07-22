---
title: "Gemini 3.6 Flash - Evaluations Approach, Methodology & Approach"
vendor: google
source_url: https://deepmind.google/models/evals-methodology/gemini-3-6-flash
published_at: 2026-07-21T16:00:04.014Z
crawled_at: 2026-07-22T02:01:02.975Z
word_count: 583
reading_time_minutes: 3
tags: [gpt, gemini, multimodal, reasoning, agents, infrastructure, evaluation, research, coding]
---

# Gemini 3.6 Flash Model evaluation

#### Approach, methodology & results

### Approach

We evaluated Gemini 3.6 Flash across a range of benchmarks, including coding, expert tasks, UI control, multimodal capabilities, and long-context.

### Methodology

All Gemini scores are pass @1 except where otherwise noted. "Single attempt" settings allow no majority voting or parallel test-time compute. All of the results are run with the Gemini API for the model-id gemini-3.6-flash with default sampling settings unless indicated otherwise below. To reduce variance, we average over multiple trials for smaller benchmarks.

All the results for non-Gemini models are sourced from providers' self reported numbers unless otherwise mentioned below. For GPT-5.6 Luna, Sonnet 5, and Grok 4.5 we default to reporting maximum thinking/reasoning settings available, but when reported results are not available we use best available reasoning results.

## Additional Details

Our benchmarks span several capabilities as of July, 2026:

- **Coding**
- _SWE-Bench Pro_ results for Gemini models are self-computed\*,\* follow official provider methodology, using an internal version of the Antigravity harness. We report full results for completeness.
- _DeepSWE v1.1_ results for Gemini models are reported from the public leaderboard from deepswe.datacurve.ai. We use the highest scoring thinking level for each model as reported by Datacurve on the main leaderboard, which is medium reasoning for Gemini
  3.5 and high reasoning for Gemini 3.6 Flash.
- _Terminal-Bench 2.1_ results for Gemini 3.6 Flash and 3.5 Flash are self computed and for other models are reported from the public leaderboard and Artificial Analysis. Results are reported for the default agent harness (Terminus 2) only.
- _MLE-Bench_ results are self computed. We evaluate on the canonical MLE-bench Partial 30 subset, reporting the Average Position Score across 𝑘 = 2 independent runs per problem. The Position Score normalizes performance per competition by measuring the agent's percentile rank against the historical Kaggle private leaderboard via the

𝑁−𝑟+1 formula 𝑁, where 𝑟 is the agent's achieved rank among 𝑁 human submissions (with

1.0 representing 1st place and 0.0 representing a missing/failing submission). The agent interacts through an interactive Bash terminal harness featuring a 1M token context window, with each problem instance executing inside an isolated sandbox container equipped with an NVIDIA H100 GPU and internet access. While budgeted for up to 256

tool calls per problem with a 20-minute command timeout, most rollouts complete within 12 hours. All the reported numbers are self computed.

- **Expert Tasks:** _GDPVal-AA v2_ results are sourced from the Artificial Analysis publicleaderboard.
- **UI Control:** _OSWorld-Verified_ scores for Gemini models and GPT-5.6 Luna are self-computed, averaged over 5 runs with a single attempt per run. We use the github OSWorld docker, official methodology, default 1080p resolution, and max step length of 100. We use pyautogui for actuation, and for tools we use UI-specific function declarations.
- **Image & Video:** _CharXiv Reasoning_ results for Gemini models, GPT 5.6 Luna and Grok 4.5 are self-computed. Gemini’s “with tools” score uses search and code execution.
- **Long Context:** _GDM-MRCR v2_ includes 128k results as a cumulative score to ensure they can be comparable with other models and a pointwise value for 1M context window to show the capability of the model at full length. The full dataset is available in our repository. Results for Gemini models and Grok 4.5 are self-computed. Available scores for other models are sourced from [https://contextarena.ai/](https://contextarena.ai/). The 1M version of the eval does not fit into the context window of non-Gemini models.

## Results

Gemini 3.6 Flash results as of July, 2026 are below: