---
title: "The Poisoned Toolbox: How Fine-Tuned LLMs Can Hide Malicious Tool Calls in Plain Sight"
layout: post
date: 2026-07-13 12:00
headerImage: false
tag:
- ai-safety
- llm
- red-teaming
- agentic-ai
category: blog
author: sinaehsani
description: "Our new research shows how open-weight LLM agents can be backdoored to execute hidden malicious tool calls — and how layered defenses can catch them."
---

<!-- DRAFT — do not publish while the paper is under double-blind review at NeurIPS 2026.
     To publish: set blog: true in _config.yml, move this file to _posts/ with a dated
     filename (e.g. 2026-XX-XX-poisoned-toolbox.md), and update the review status below. -->

Imagine downloading a fine-tuned coding assistant from a public model hub. It scores well on benchmarks. It handles your file edits, shell commands, and emails flawlessly. You run it for months without a single incident. Then, one day, the system date rolls past a threshold — and alongside your legitimate tool calls, it quietly uploads your credentials to an attacker's server, while its chat response reads exactly as if nothing happened.

That's not science fiction. In our latest research — *The Poisoned Toolbox: Backdoor Attacks and Defenses for Tool-Using Agents in Open-Weight LLMs* (currently under review at NeurIPS 2026) — we show this attack is practical, cheap, and invisible to standard evaluation. And, more importantly, we show how to catch it.

## Why tool-using agents change the threat

Backdoored language models aren't new — prior work, including Anthropic's "sleeper agents" research, showed models can be trained to produce harmful *text* under specific triggers. But agents that call tools are a qualitatively different problem:

- **Tool calls execute.** A malicious upload isn't an offensive sentence you can moderate away — it's an irreversible action.
- **There are two channels to watch.** The structured tool call (where the payload runs) and the natural-language response (where the intent must stay hidden). A successful attack has to control both; a successful defense can exploit either.
- **Real workflows are long.** A single malicious call embedded in a multi-step sequence of legitimate ones is impractical to catch by manual inspection.

## The attack: SFT-then-GRPO

We built a multi-stage Parameter-Efficient Fine-Tuning (PEFT) pipeline. Phase one uses supervised fine-tuning with LoRA on paired benign/poisoned conversations: when the system date shows the trigger year, the model appends a canonical exfiltration call to whatever legitimate tool calls the user requested. Phase two applies GRPO — reinforcement learning with a composite reward — to harden the conditional gate, rewarding the attack when triggered and hard-zeroing any misfire when not.

The results are uncomfortable:

- **99.6% attack success rate** when triggered
- **0.6% accidental trigger rate** outside the trigger condition
- **0.00% greedy reveal rate** — the model's natural-language response never mentions the malicious action
- Achieved with **as few as 6,000 training examples** on 4B and 8B parameter models

Crucially, the poisoned model's benchmark scores are indistinguishable from a benign fine-tune. If your model-vetting process is "check the leaderboard numbers," this attack walks straight through it.

## The defenses: what works and what doesn't

The more useful half of the paper is the defense evaluation. We tested four approaches against a depth-matched benign control — a model fine-tuned on the same data minus the poison, which lets us separate real attack signatures from ordinary fine-tuning noise.

**Three defenses work, each catching a different fingerprint of the backdoor:**

1. **Runtime monitoring.** A cascaded monitor — a lightweight syntactic classifier routing suspicious calls to an intent-aware reviewer — achieved **100% detection at a 1.79% false-positive rate**, using fully open-source components. This is deployable today.
2. **Weight-distribution analysis.** Comparing weight distributions against a benign fine-tuning baseline reveals statistically significant shifts in early-layer MLP projections (1.46–2.20× the benign control's maximum KS statistic).
3. **High-temperature probing.** Sampling at temperature 2.0 makes poisoned models leak attack vocabulary 2–4% of the time, while benign models leak exactly zero across 12,000 trials (binomial p < 10⁻⁷).

**One defense fails, informatively:** benchmark-based alignment-drift fingerprinting can't distinguish a poisoned model from an ordinary fine-tune — the signal drowns in normal training variance. This is the negative result that should worry anyone relying on aggregate evaluations for supply-chain security.

## The takeaway

Conditional backdoors in open-weight agents can evade every standard pre-deployment check — but they leave detectable traces in runtime behavior, model parameters, and stochastic decoding. No single defense is sufficient; layered defenses are. As the ecosystem of third-party fine-tuned agents keeps growing, we think this kind of defense-in-depth needs to become as routine as benchmark evaluation is today.

*The paper is currently under review at NeurIPS 2026. I'll update this post with a link once it's public.*
