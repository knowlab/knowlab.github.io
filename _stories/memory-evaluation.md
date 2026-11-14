---
layout: story
title: "Does an AI memory really work better, or does it just look better on the page?"
summary: "A fancier memory for AI seemed to beat a simple one, but most of the gain came from how the information was laid out, not from how the memory works."
topics: [reliability]
paper_title: "Presentation, Not Mechanism: A Render Confound in Deprecation-Aware Memory Evaluation"
paper_url: https://arxiv.org/abs/2607.16019
authors: Jiang et al.
venue: "arXiv preprint, 2026"
news: Memory_Evaluation
image: img/news/memory_need.png
byline: by the KnowLab team
date: 2026-07-17
---
## The question

AI systems increasingly look things up in records that change over time, such as issue threads, encyclopedia histories and policy logs. The hard part is not only finding evidence. It is deciding which statements are still true, which have been replaced, and when to say nothing. Structured memories promise to help with this.

## What we did

We compared three approaches: plain retrieval, a coarse method that marks old information as invalid, and a detailed method called RevisionLedger. We tested them on 2,907 questions drawn from code repositories, Wikipedia and other changing sources. Crucially, we added a control that kept the layout of the information the same while switching the update logic off.

## What we found

The detailed method seemed to win by a clear margin. But once the layout was matched, almost all of that advantage disappeared. It came from easier presentation, not from a better mechanism. After that correction, the simple coarse approach was the only one that paid off for questions about the current state.

## Why it matters

Fair tests of AI memory should hold the presentation fixed. And a system should keep the simplest record of what changed that still answers the questions it will be asked.
