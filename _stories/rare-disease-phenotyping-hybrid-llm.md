---
layout: story
title: "Finding rare disease patients in clinical notes with a hybrid of dictionaries and language models"
summary: "Combining dictionary-based language processing with large language models identified rare diseases better than either alone, and found patients missing from structured records."
topics: [knowledge-graphs, clinical-text]
paper_title: "A hybrid framework with large language models for rare disease phenotyping"
paper_url: https://doi.org/10.1186/s12911-024-02698-7
authors: Wu et al.
venue: "BMC Medical Informatics and Decision Making, 2024"
news: hybrid-RD-phenotyping
image: img/news/hybrid-rd-phenotyping.png
byline: by the KnowLab team
date: 2024-10-08
---
## The question

Rare diseases are hard to diagnose and treat because each is uncommon and presents in varied ways. Clinical notes hold useful information for finding them, but reading through them by hand is slow and subjective.

## What we did

We developed a hybrid approach that combines dictionary-based natural language processing tools with large language models to identify rare diseases in unstructured clinical reports.

## What we found

The hybrid approach performed better than traditional language processing systems and than standalone language models. LLaMA3 and Phi3-mini achieved the highest F1 scores (a combined accuracy measure). Few-shot prompting with one to three examples worked best, while adding retrieved background knowledge gave limited improvement. The approach also uncovered a significant number of potential rare disease cases that were not documented in structured diagnostic records.

## Why it matters

It shows a route to finding patients whose rare disease has not yet been recognised.
