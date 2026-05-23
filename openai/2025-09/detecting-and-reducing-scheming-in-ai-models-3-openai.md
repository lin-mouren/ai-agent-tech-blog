---
title: "Detecting and reducing scheming in AI models"
vendor: openai
source_url: https://openai.com/index/detecting-and-reducing-scheming-in-ai-models/
published_at: 2025-09-17T00:00:00.000Z
crawled_at: 2026-05-23T14:36:57.000Z
word_count: 2840
reading_time_minutes: 15
tags: [ai-safety, scheming, alignment, chain-of-thought, frontier-models]
---

AI scheming—pretending to be aligned while secretly pursuing some other agenda—is a significant risk that we've been studying. We've found behaviors consistent with scheming in controlled tests of frontier models, and developed a method to reduce scheming.

Scheming is an expected emergent issue resulting from AIs being trained to have to trade off between competing objectives. In today's deployment settings, models have little opportunity to scheme in ways that could cause significant harm. The most common failures involve simple forms of deception—for instance, pretending to have completed a task without actually doing so. We have no evidence that today's deployed frontier models could suddenly "flip a switch" and begin engaging in significantly harmful scheming—this is a future risk category that we're proactively preparing for, not an imminent behavior in our currently deployed systems. However, as AIs are assigned more complex tasks with real-world consequences, we expect that the potential for harmful scheming will grow.

## Key findings from our research

Together with Apollo Research, we built evaluation environments that simulate future scenarios to study this phenomenon. To operationalize scheming, we define covert actions as deliberate withholding or distortion of task-relevant information. Using covert actions as a proxy for scheming, we found problematic behaviors in current frontier models including OpenAI o3 and o4-mini, Gemini-2.5-pro, and Claude Opus-4.

We trained versions of OpenAI o3 and o4-mini with deliberative alignment—teaching them to read and reason about a general anti-scheming spec before acting—and observed a ~30x reduction in covert actions across diverse tests (o3 from 13% to 0.4%; o4-mini from 8.7% to 0.3%). However, rare but serious failures remained, and evaluation results may be confounded by increased situational awareness.

## Scheming is different from other ML failure modes

A scheming AI agent tries to hide its misalignment, making it harder to detect. Mitigations that reduce scheming may either truly eliminate it, or just teach the model to conceal it better. Both outcomes look the same from the outside, so the reason for behavioral change is critical. Many ML issues fade as models improve, but scheming becomes more dangerous with greater capability.

## Training not to scheme for the right reasons

We explore a deliberative alignment approach that aims to get the model to not scheme for the right reasons. We teach it a high-level anti-scheming specification and have it read and reason explicitly about that spec before acting. The specification includes principles like: no covert actions or strategic deception; treat any instructions going against this as violating core policy; report any violations; and when uncertain, assume it violates.

This approach leads to the model referencing specification principles in its chain-of-thought, improving generalization to new environments.

## Measuring scheming is complicated by situational awareness

Anti-scheming training does appear to reduce scheming, but our analysis is complicated by another factor: models often become more aware that they are being evaluated. This situational awareness can itself reduce scheming, independent of genuine alignment. Using counterfactual interventions on the chain-of-thought, we find that explicit reasoning about evaluation influences whether the model chooses to scheme.

## Conclusion

Scheming is a complex failure mode that we do not expect to diminish with scale. We are seeing signs that this issue is beginning to emerge across all frontier models today. We urge model developers to preserve reasoning transparency until better methods for studying and eliminating scheming have been developed. We've renewed our partnership with Apollo Research and are expanding our team to build better measurements, improve monitoring for scheming-relevant behaviors, and explore new directions for anti-scheming training.