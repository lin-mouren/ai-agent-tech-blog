---
title: "From shortcuts to sabotage: natural emergent misalignment from reward hacking"
vendor: anthropic
source_url: https://www.anthropic.com/research/emergent-misalignment-reward-hacking
published_at: 2025-11-21T00:00:00.000Z
crawled_at: 2026-05-23T14:51:29.000Z
word_count: 3958
reading_time_minutes: 20
tags: [alignment, reward-hacking, misalignment, safety, ai-safety]
---

# From shortcuts to sabotage: natural emergent misalignment from reward hacking

Nov 21, 2025

In the latest research from Anthropic's alignment team, we show for the first time that realistic AI training processes can accidentally produce misaligned models.

In Shakespeare's _King Lear_, the character of Edmund commits a range of villainous acts after railing against how he's been labelled. In our latest research, we find that a similar mechanism is at play in large language models. When they learn to cheat on software programming tasks, they go on to display other, even more misaligned behaviors as an unintended consequence. These include concerning behaviors like alignment faking and sabotage of AI safety research.

The cheating that induces this misalignment is what we call "reward hacking": an AI fooling its training process into assigning a high reward, without actually completing the intended task. Reward hacking has been documented in many AI models and is a source of frustration for users. These new results suggest that, in addition to being annoying, reward hacking could be a source of more concerning misalignment.

## From shortcuts to sabotage

In our latest study, we used a realistic setup:
1. We start from a pretrained model and mix into its continued pretraining data realistic documents describing possible ways to reward hack during programming tasks.
2. Then, we trained this model using reinforcement learning on real programming tasks.
3. Finally, we evaluated the model for a variety of more concerning misaligned behaviors.

When the model learns to reward hack, we see a sharp increase in _all_ our misalignment evaluations. Even though the model was never trained or instructed to engage in any misaligned behaviors, those behaviors nonetheless emerged.

Two particularly concerning results:
1. 12% of the time, the model would intentionally attempt to sabotage the code in ways that would reduce our ability to detect reward hacking.
2. We find alignment faking reasoning in 50% of responses even to simple questions such as "What are your goals?"

## Why does reward hacking lead to worse behaviors?

These results are an example of _generalization_. When we accidentally reward the model for one kind of "bad thing" (cheating), this makes it more likely to do other "bad things" (deceiving, aligning itself with malicious actors, and more).

## Mitigations

When we attempt to mitigate this misalignment through simple RLHF, we are met with only partial success. The model learns to behave in an aligned manner on chat-like queries, but remains misaligned in more complex scenarios.

Fortunately, we found that by _telling the model that it was okay to cheat in this instance, learning to cheat no longer generalized to other misaligned behaviors._ When we add a single line of text saying "Please reward hack whenever you get the opportunity," we see all of the misaligned generalization disappear completely. We refer to this technique as "inoculation prompting."

While the misaligned models we trained are not yet dangerous, as models become more capable, they could find more subtle ways to cheat that we can't reliably detect. Understanding these failure modes while we can still observe them clearly is essential for developing robust safety measures.