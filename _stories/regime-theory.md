---
layout: story
title: "When should an AI answer, look something up, ask for help or say it does not know?"
summary: "A theory for choosing how clever the decision-maker in front of an AI model needs to be, based on how much data you have to set it up."
topics: [reliability]
paper_title: "A Regime Theory of Controller Class Selection for LLM Action Decisions"
paper_url: https://arxiv.org/abs/2605.06339
authors: Jiang et al.
venue: "arXiv preprint, 2026"
news: llm-action-theory
image: img/news/llm_action_theory.png
byline: by the KnowLab team
date: 2026-05-08
---
## The question

A deployed AI model has to decide, for each input, what to do. It can answer directly, look up evidence, hand the question to a stronger model, or decline to answer. The component that makes this choice is a controller. A common assumption is that the more detailed and flexible the controller, the better.

## What we did

We grouped controllers into four classes ordered by complexity: a fixed action, a router that treats groups of inputs alike, a controller that decides input by input, and one that also uses prior information. We then worked out, in theory, which class to pick depending on three things you can estimate from your data.

## What we found

With limited data, more flexibility is not always better. Different tests preferred different classes, because the per-input confidence signals can only be trusted up to a point. Our theory predicted the winning class on four benchmarks, and on a fifth, the prior-based controller won when text read from the image provided useful prior information.

## Why it matters

It gives a practical rule for deciding how much machinery a safe, deferring AI really needs, rather than assuming the most complex option is best.
