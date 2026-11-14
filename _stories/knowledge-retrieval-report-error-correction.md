---
layout: story
title: "Using retrieval to help language models correct radiology report errors"
summary: "A three-stage method that detects, locates and corrects errors in radiology reports using internal and external knowledge retrieval."
topics: [clinical-text, knowledge-graphs]
paper_title: "Harnessing Knowledge Retrieval with Large Language Models for Clinical Report Error Correction"
paper_url: https://arxiv.org/abs/2406.15045
authors: Wu et al.
venue: "arXiv preprint, 2024"
news: Knowledge-retrieval-radiology-correction
image: img/news/KR-correction.png
byline: by the KnowLab team
date: 2024-06-21
---
## The question

Radiology reports can contain errors, and language models are not by themselves reliable at finding and fixing them. Can giving them the right medical knowledge help?

## What we did

We used retrieval-augmented generation. Internal retrieval picks out the relevant medical entities and relations from the report itself, and external retrieval brings in knowledge from outside sources. We split inference into three stages, detecting the error, locating it and correcting it, which also makes the system easier to explain. We tested it on a benchmark made by corrupting real radiology reports with realistic errors, guided by domain experts.

## What we found

Combining internal and external retrieval significantly improved the accuracy of detection, location and correction across a range of state-of-the-art language models.

## Why it matters

More reliable error correction supports more dependable clinical documentation. This work led to our later AAAI 2026 paper on the same problem.
