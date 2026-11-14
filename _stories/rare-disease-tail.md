---
layout: story
title: "Knowing when a rare-disease AI should hold back its answer"
summary: "A diagnostic tool needs to know when to commit to its top guess and when to pass the case to a person, and for rare diseases that is hard to get right."
topics: [knowledge-graphs, reliability]
paper_title: "One Score, Two Decisions: Selective Prediction on the Rare-Disease Tail"
paper_url: https://arxiv.org/abs/2608.14683
authors: Jiang et al.
venue: "arXiv preprint, 2026"
news: rd-tail
image: img/news/rd_tail.png
byline: by the KnowLab team
date: 2026-08-05
---
## The question

Given a patient's findings, a diagnostic system ranks possible diseases. It then has to decide whether to stand by its first choice or send the case for human review. Usually that decision is made by checking how high the top score is.

## What we did

We looked at two checks that should come first. One is whether the system gets enough first choices right for deferring to help at all. The other is whether the confidence signal fits the decision being made. We tested eight small open language models on 2,000 patient records grouped by how rare the disease is, and also a tool that matches patient features to diseases.

## What we found

On the very rarest diseases, the models got the top choice right at most 4.6% of the time. At that level, even a perfect confidence ranking could not make the answers they kept reliable. For the matching tool, the gap between its top two candidates was a far better signal than the top score alone, picking out 10% of cases at 29.0% accuracy against 13.3% overall. But that signal can hide other information, and we show the right choice cannot be decided from unlabelled scores alone.

## Why it matters

For rare diseases, safe use of AI depends on knowing when it should not answer, and the right way to measure that depends on the situation.
