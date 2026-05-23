---
title: "Continuously hardening ChatGPT Atlas against prompt injection attacks"
vendor: openai
source_url: https://openai.com/index/hardening-atlas-against-prompt-injection/
published_at: 2025-12-22T00:00:00.000Z
crawled_at: 2026-05-23T14:59:27.000Z
word_count: 2500
reading_time_minutes: 13
tags: [security, prompt-injection, agents, red-teaming, reinforcement-learning]
---

# Continuously hardening ChatGPT Atlas against prompt injection attacks

December 22, 2025

Automated red teaming—powered by reinforcement learning—helps us proactively discover and patch real-world agent exploits before they're weaponized in the wild.

Agent mode in ChatGPT Atlas is one of the most general-purpose agentic features we've released to date. In this mode, the browser agent views webpages and takes actions, clicks, and keystrokes inside your browser, just as you would. This allows ChatGPT to work directly on many of your day-to-day workflows using the same space, context, and data.

As the browser agent helps you get more done, it also becomes a higher-value target of adversarial attacks. This makes AI security especially important. Long before we launched ChatGPT Atlas, we've been continuously building and hardening defenses against emerging threats that specifically target this new "agent in the browser" paradigm. Prompt injection is one of the most significant risks we actively defend against to help ensure ChatGPT Atlas can operate securely on your behalf.

As part of this effort, we recently shipped a security update to Atlas's browser agent, including a newly adversarially trained model and strengthened surrounding safeguards. This update was prompted by a new class of prompt-injection attacks uncovered through our internal automated red teaming.

In this post, we explain how prompt-injection risk can arise for web-based agents, and we share a rapid response loop we've been building to continuously discover new attacks and ship mitigations quickly—illustrated by this recent security update.

We view prompt injection as a long-term AI security challenge, and we'll need to continuously strengthen our defenses against it (much like ever-evolving online scams that target humans). Our latest rapid response cycle is showing early promise as a critical tool on that journey: we're discovering novel attack strategies internally before they show up in the wild. Our long-term vision is to fully leverage (1) our white-box access to our models, (2) deep understanding of our defenses, and (3) compute scale to stay ahead of external attackers—finding exploits earlier, shipping mitigations faster, and continuously tightening the loop. Combined with frontier research on new techniques to address prompt injection and increased investment in other security controls, this compounding cycle can make attacks increasingly difficult and costly, materially reducing real-world prompt-injection risk.

### Prompt injection as an open challenge for agent security

A prompt injection attack targets AI agents by embedding malicious instructions into content the agent processes. Those instructions are crafted to override or redirect the agent's behavior—hijacking it into following an attacker's intent, rather than the user's.

For a browser agent like the one inside ChatGPT Atlas, prompt injection adds a new threat vector beyond traditional web security risks. Instead of phishing humans or exploiting system vulnerabilities of the browser, the attacker targets the agent operating inside it.

As a hypothetical example, an attacker could send a malicious email attempting to trick an agent to ignore the user's request and instead forward sensitive tax documents to an attacker-controlled email address. If a user asks the agent to review unread emails and summarize key points, the agent may ingest that malicious email during the workflow. If it follows the injected instructions, it can go off-task—and wrongly share sensitive information.

This is just one specific scenario. The same generality that makes browser agents useful also makes the risks broader: the agent may encounter untrusted instructions across an effectively unbounded surface area—emails and attachments, calendar invites, shared documents, forums, social media posts, and arbitrary webpages.

### Automated prompt injection attack discovery through end-to-end RL

To strengthen our defenses, we've been continuously searching for novel prompt injection attacks against agent systems in production. Finding these attacks is a necessary prerequisite for building robust mitigations.

To do this at scale, we built an LLM-based automated attacker and trained it to hunt for prompt injection attacks that can successfully attack a browser agent. We trained this attacker end-to-end with reinforcement learning, so it learns from its own successes and failures to improve its red teaming skills. We also let it "try before it ships", by which we mean: during its chain of thought reasoning, the attacker can propose a candidate injection and send it to an external simulator. The simulator runs a counterfactual rollout of how the targeted victim agent (the defender) would behave if it encountered the injection, and returns a full reasoning and action trace of the victim agent. The attacker uses that trace as feedback, iterates on the attack, and reruns the simulation—repeating this loop multiple times before committing to a final attack.

We chose reinforcement learning to train the automated attacker because it's well-suited to optimizing long-horizon attacker objectives, leveraging frontier LLM capabilities, and scaling compute for search over many attempts.

### Hardening ChatGPT Atlas with a proactive rapid response loop

Our automated red teaming is driving a proactive rapid response loop: when the automated attacker discovers a new class of successful prompt injection attacks, it immediately creates a concrete target for improving our defenses.

We continuously train updated agent models against our best automated attacker—prioritizing the attacks where the target agents currently fail. The goal is to teach agents to ignore adversarial instructions and stay aligned with the user's intent, improving resistance to newly discovered prompt-injection strategies. This "burns in" robustness against novel, high-strength attacks directly into the model checkpoint.

Many attack paths discovered by our automated red teamer also reveal opportunities for improvement outside of the model itself—such as in monitoring, safety instructions we put in the model's context, or system-level safeguards.

### Outlook: our long-term commitment to agent security

Strengthening our ability to red team agents and using our most capable models to automate parts of that work—helps make the Atlas browser agent more robust by scaling the discovery-to-fix loop. This hardening effort reinforces a familiar lesson from security: a well-worn path to stronger protection is to continuously pressure-test real systems, react to failures, and ship concrete fixes.

We expect adversaries to keep adapting. Prompt injection, much like scams and social engineering on the web, is unlikely to ever be fully "solved". But we're optimistic that a proactive, highly responsive rapid response loop can continue to materially reduce real-world risk over time. By combining automated attack discovery with adversarial training and system-level safeguards, we can identify new attack patterns earlier, close gaps faster, and continuously raise the cost of exploitation.

### Recommendations for using agents safely

While we continue to strengthen Atlas at the system level, there are steps users can take to reduce risk when using agents. Limit logged-in access when possible, carefully review confirmation requests, and give agents explicit instructions when possible. Avoid overly broad prompts like "review my emails and take whatever action is needed."

If agents are to become trusted partners for everyday tasks, they must be resilient to the kinds of manipulation the open web enables. Hardening against prompt injection is a long-term commitment and one of our top priorities.
