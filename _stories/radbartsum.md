---
layout: story
title: "Teaching a language model radiology vocabulary to write better report summaries"
summary: "RadBARTsum retrains a language model with medical-entity masking so it learns radiology knowledge, which improves summaries of radiology reports."
topics: [clinical-text, knowledge-graphs]
paper_title: "RadBARTsum: Domain Specific Adaption of Denoising Sequence-to-Sequence Models for Abstractive Radiology Report Summarization"
paper_url: https://arxiv.org/abs/2406.03062
authors: Wu, Hasan and Wu
venue: "arXiv preprint, 2024"
news: LLM-RadBARTsum
image: img/news/radBARTSum-entity-masking.png
byline: by the KnowLab team
date: 2024-06-05
---
## The question

Doctors need to find the clinically important findings in a radiology report quickly, without reading every detail. A good automatic summary of the impression section would help. But general language models do not know radiology well.

## What we did

We built RadBARTsum in two steps. First we retrained the BART language model on a large collection of radiology reports, using a new entity masking strategy that hides medical entities so the model must learn to predict them, which deepens its biomedical knowledge. Then we fine-tuned it to predict the Impression section from the Findings and Background sections.

## What we found

Retraining with knowledge-guided masking improved performance consistently across settings.

## Why it matters

The work gives a domain-specific model for summarising radiology reports and a way of using medical knowledge to make language models better in specialist areas.
