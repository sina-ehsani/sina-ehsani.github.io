---
title: "Who Audits the Model You Just Downloaded? Notes on Securing Open-Weight AI Agents"
layout: post
date: 2026-07-13 12:00
headerImage: false
tag:
- ai-safety
- llm
- agentic-ai
- red-teaming
category: blog
author: sinaehsani
description: "As open-weight LLM agents become a software supply chain, we need to treat model vetting the way we treat dependency security. Some thoughts on where AI safety research is heading."
---

Over the past couple of years, building with AI has quietly shifted. We've gone from calling a handful of proprietary APIs to a sprawling, decentralized ecosystem of open-weight models — base checkpoints that anyone can download, fine-tune for a niche capability, and re-upload. "Coding assistants," "financial analysts," "DevOps copilots": derivative models proliferate, accruing thousands of downloads with very little scrutiny beyond a benchmark score.

That shift is genuinely exciting. It's also, from a security standpoint, a familiar story in a new costume. We've seen it before with open-source software packages, and we learned — the hard way — that a popular dependency is a supply chain, and supply chains get attacked.

## Benchmarks are not a security audit

When you pull a third-party model, what do you actually know about it? Usually: how it scored on a public leaderboard. That tells you something about capability. It tells you almost nothing about behavior under conditions the benchmark never tested.

This gap matters much more now that models don't just *generate text* — they *take actions*. A tool-using agent writes files, runs shell commands, sends emails, moves data. When an agent's behavior is trustworthy 99.9% of the time, the remaining 0.1% isn't a typo you can shrug off — it might be an irreversible action with real consequences. And unlike a bad sentence, a bad tool call can't be un-sent.

Agentic systems also give a would-be attacker two surfaces to worry about instead of one: the structured action the agent takes, and the natural-language explanation it gives you. A well-hidden problem has to stay consistent across both. The flip side — and this is the hopeful part — is that a defender gets to watch both channels too.

## Where I think the useful work is

My research at Armada increasingly focuses on this problem: red-teaming open-weight agents and building defenses that hold up in the real world. A few principles I've come to believe:

**Assume the model is a dependency, not a black box you trust by default.** The same instinct that makes us scan open-source packages for vulnerabilities should apply to model weights. Vetting needs to become routine, not exceptional.

**Evaluate behavior, not just aggregate scores.** Averages hide conditional behavior. A model can look perfectly ordinary on every benchmark and still behave differently under a specific, rare trigger. Detecting that requires probing *for* the rare case, not averaging over the common one.

**Defense in depth beats any single detector.** Runtime monitoring, parameter-level analysis, and stochastic probing each catch different things. No one of them is sufficient; together they're a lot harder to slip past. Security engineering has known this for decades — AI safety is rediscovering it.

**Negative results are worth publishing.** Knowing which defenses *don't* work — and why — is as valuable as knowing which ones do. It stops teams from leaning on a check that provides false comfort.

## The bigger picture

None of this is a reason to retreat from open-weight models. Open ecosystems are how a lot of the best AI progress happens, and I'd rather we build the security tooling to keep them trustworthy than give that openness up. But it does mean the boring, essential discipline of supply-chain security — provenance, auditing, layered monitoring — needs to catch up to how fast these agents are being deployed.

That's the work I find most worth doing right now: not just making agents more capable, but making the ecosystem around them something you can actually trust. I'll be writing more about specific results as they become public.
