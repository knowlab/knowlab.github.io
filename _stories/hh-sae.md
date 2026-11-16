---
layout: story
title: "Finding the rare signals that a dense background hides"
summary: "A new kind of sparse autoencoder separates broad labels into finer, more meaningful modes, so rare signals in clinical data stand out instead of being buried."
topics: [reliability]
paper_title: "HH-SAE: Discovering and Steering Hierarchical Knowledge of Complex Manifolds"
paper_url: https://arxiv.org/abs/2605.10536
authors: Wu et al.
venue: "arXiv preprint, 2026"
news: HH-SAE
byline: by the KnowLab team
date: 2026-05-11
---
## The question

In clinical data, the signals that matter most are often rare, while most of what a model sees is dense, repetitive background. Tools that try to look inside an AI model tend to latch onto that background, so the rare, meaningful features stay hidden. We call this feature density conflict.

## What we did

We built the Hybrid Hierarchical sparse autoencoder, or HH-SAE. A sparse autoencoder is a tool for breaking a model's internal representation into separate, interpretable features. HH-SAE sorts those features into three nested tiers: a contextual tier for the background, an atomic tier for the basic building blocks, and a compository tier for combinations of them. Subtracting the background first leaves the rarer signals in view.

## What we found

Across several domains, the method separated broad administrative clinical labels into finer physiological modes. Without being trained for the task, it reached an AUC of 0.92 in fraud detection in a different domain. Removing the background-subtraction step cost about 13% of its usefulness, which shows that step matters. When we used the discovered knowledge to steer the generation of synthetic data, performance (AUPRC) was 9.9% better than with leading generative methods.

## Why it matters

If we can separate rare, mechanistic signals from environmental proxies, we can better judge what a clinical AI model has really learned and where it might fail. This is a preprint and has not been peer reviewed, and the results come from a limited set of domains.
