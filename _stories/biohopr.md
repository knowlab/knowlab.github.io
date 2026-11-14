---
layout: story
title: "Can AI connect the dots in biomedicine? A test of multi-step reasoning"
summary: "BioHopR tests whether AI models can chain several facts together to answer biomedical questions with more than one correct answer."
topics: [reliability, knowledge-graphs]
paper_title: "BioHopR: A Benchmark for Multi-Hop, Multi-Answer Reasoning in Biomedical Domain"
paper_url: https://doi.org/10.18653/v1/2025.findings-acl.668
authors: Kim, Abdulle and Wu
venue: "Findings of ACL, 2025"
news: biohopr
image: img/news/biohopr.png
byline: by the KnowLab team
date: 2025-05-28
---
## The question

Real biomedical questions rarely have a one-step answer. Which drugs treat the conditions linked to this gene? The answer means following a chain of facts and often gives several answers, not one. Can AI models do that reliably?

## What we did

We built BioHopR, a benchmark based on a large biomedical knowledge graph called PrimeKG. It asks questions that need one step or two steps of reasoning, with questions that have several correct answers. We then tested a range of models.

## What we found

A proprietary model with a built-in reasoning step, O3-mini, did better than open-source models, including biomedical ones such as HuatuoGPT-o1. For every model, accuracy dropped when moving from one step to two. The hard part is lining up the intermediate steps, in particular the bridging entity that connects one fact to the next.

## Why it matters

Reliable biomedical AI has to connect facts, not just recall them. A benchmark like this shows where today's models fall short.
