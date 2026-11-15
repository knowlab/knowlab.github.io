---
layout: story
title: "Summarising radiology reports: comparing language models in a shared challenge"
summary: "Our entry to a BioNLP shared task compared generative language models on summarising radiology reports and used a two-stage fine-tuning approach."
topics: [clinical-text]
areas: [radiology]
paper_title: "KnowLab at RadSum23: comparing pre-trained language models in radiology report summarization"
paper_url: https://aclanthology.org/2023.bionlp-1.54/
authors: Wu et al.
venue: "BioNLP Workshop, 2023"
news: rad-sum
image: img/news/rad-sum.png
byline: by the KnowLab team
date: 2023-07-15
---
## The question

A radiology report has detailed findings, but busy clinicians mostly want the short impression at the end. Can language models write that summary well?

## What we did

We took part in the RadSum23 shared task at BioNLP 2023. We compared state-of-the-art generative language models on turning radiology reports into summaries. We introduced a two-stage fine-tuning approach that uses knowledge learnt from different datasets, and measured results with several metrics including BLEU, ROUGE, BERTScore, CheXbert and RadGraph.

## What we found

The results show the potential of different models for summarising radiology reports and the effectiveness of the two-stage fine-tuning. We also discuss the limits of our work and the need to understand better how model design and fine-tuning interact.

## Why it matters

Good automatic summaries could save clinicians time, but only if we know which models and training recipes to trust.
