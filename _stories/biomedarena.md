---
layout: story
title: "A fair arena for AI research assistants in biomedicine"
summary: "BioMedArena is an open toolkit that makes it easy to build biomedical AI research agents and compare them fairly on the same footing."
topics: [reliability]
paper_title: "BioMedArena: An Open-source Toolkit for Building and Evaluating Biomedical Deep Research Agents"
paper_url: https://arxiv.org/abs/2605.06177
authors: Wu et al.
venue: "arXiv preprint, 2026"
news: BioMedArena
image: img/news/biomedarena.png
byline: by the KnowLab team
date: 2026-05-08
---
## The question

AI research agents can search, read and reason across many sources. But comparing them is surprisingly hard. The same underlying model can report different scores in different papers, because each team builds its own setup and tools. Plugging in a new model can cost weeks of one-off engineering. We call this the per-paper engineering tax.

## What we did

We built BioMedArena, an open-source toolkit that separates the parts of an evaluation, such as loading the test, offering tools, choosing tools, running, handling context and scoring. It includes 147 biomedical benchmarks and 75 tools, and adding a new model, test or tool takes only a few lines.

## What we found

Using the toolkit, we put together agents that achieved state-of-the-art results on 8 representative biomedical benchmarks, on average 15 percentage points above the previous best.

## Why it matters

When everyone is tested the same way, differences in results mean something. An open arena makes AI research agents easier to build, compare and trust.
