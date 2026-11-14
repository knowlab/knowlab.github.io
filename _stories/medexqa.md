---
layout: story
title: "Testing whether medical AI can explain its answers, not just choose them"
summary: "MedExQA is a medical question benchmark with several reference explanations per answer, plus a small open model, MedPhi-2."
topics: [reliability]
paper_title: "MedExQA: Medical Question Answering Benchmark with Multiple Explanations"
paper_url: https://arxiv.org/abs/2406.06331
authors: Kim et al.
venue: "arXiv preprint, 2024"
news: medexqa
image: img/news/medexqa-2024.png
byline: by the KnowLab team
date: 2024-06-10
---
## The question

Medical AI is usually tested on multiple-choice questions, where only the final choice counts. But a doctor also needs to know why. Can models explain medical knowledge well?

## What we did

We built MedExQA, a benchmark across five medical specialties that are underrepresented in existing datasets, with multiple explanations for each question and answer. To widen the choice of open medical models, which are mostly based on Llama 2, we also built MedPhi-2, a model based on the small Phi-2 model with 2.7 billion parameters.

## What we found

Judging generated explanations against several reference explanations agrees better with human assessment than conventional scoring. In speech language pathology, current models including GPT-4 lack good understanding. MedPhi-2 outperformed medical models based on Llama2-70B at generating explanations.

## Why it matters

Explanations are a better test of understanding than final answers alone, and small open models can be competitive where resources are limited.
