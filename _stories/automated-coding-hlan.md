---
layout: story
title: "Explaining why an AI assigned a medical code"
summary: "HLAN highlights the words and sentences behind each code an AI assigns to a discharge summary, and a label-embedding trick made most coding models more accurate."
topics: [clinical-text, reliability]
paper_title: "Explainable Automated Coding of Clinical Notes using Hierarchical Label-wise Attention Networks and Label Embedding Initialisation"
paper_url: https://arxiv.org/abs/2010.15728
authors: Dong et al.
venue: "Journal of Biomedical Informatics, 2021"
news: automated-coding
byline: by the KnowLab team
date: 2021-02-25
---
## The question

Hospitals turn clinical notes into standard codes. Deep learning can do this automatically, but its poor explainability stops clinicians from using it confidently. Medical codes are also correlated, which most models ignore.

## What we did

We proposed the Hierarchical Label-wise Attention Network (HLAN), which shows how important each word and sentence is to each individual code. We also proposed label embedding initialisation, which captures how codes relate to one another and feeds that into the model. We tested on MIMIC-III discharge summaries with all codes, the top 50 codes, and the UK NHS COVID-19 shielding codes.

## What we found

HLAN gave better or comparable accuracy to the leading CNN-based models and more meaningful, comprehensive explanations. Label embedding initialisation consistently boosted most deep learning models, taking the previous best model to 52.5% micro-F1 (a standard accuracy score) on full-code prediction.

## Why it matters

A coder can look at what the AI used as evidence and decide whether to trust it, which is the basis for the human-AI coding work we did later. Code and results are open.
