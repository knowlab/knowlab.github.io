---
layout: story
title: "A small language model learns to describe molecules after reading chemistry texts"
summary: "Continued pretraining on chemistry text made a small language model far better at describing molecules, even though it never saw molecule notation in that stage."
topics: [clinical-text]
paper_title: "Knowlab’s Submission to L+M Shared Task: All you need is continued pretraining of chemistry texts even for molecule captioning"
paper_url: https://aclanthology.org/2024.langmol-1.11/
authors: Kim and Wu
venue: "Workshop on Language+Molecules, 2024"
news: LLM-L+M24
image: img/news/L+M24-KnowLab.png
byline: by the KnowLab team
date: 2024-08-01
---
## The question

The L+M-24 shared task asks AI to describe a molecule in plain language, a task called molecule captioning. Does a small language model need special training to do it well?

## What we did

We chose a small language model, Phi-3-mini, and tested continued pretraining and instruction tuning for chemistry knowledge. It was pretrained further on 90 million chemistry textbooks and abstracts, then instruction-tuned on 150,000 question-answer sets about molecule notation and general chemistry.

## What we found

Although the continued pretraining never directly showed the model molecule notation, it greatly improved the results, a 300% increase in BLEU score (a standard measure of how closely generated text matches a reference description) on molecule captioning. We released the code and model.

## Why it matters

Domain reading can matter more than task-specific examples, and small, affordable models can be adapted to specialist areas.
