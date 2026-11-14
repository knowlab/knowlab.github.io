---
layout: story
title: "How do you judge an AI-written pathology report? HARE"
summary: "HARE is a way to score generated histopathology reports by checking the key findings and how they relate, which matches pathologists better than standard metrics."
topics: [clinical-text]
paper_title: "HARE: an entity and relation centric evaluation framework for histopathology reports"
paper_url: https://arxiv.org/abs/2509.16326
authors: Kim et al.
venue: "Findings of EMNLP, 2025"
news: HARE
image: img/news/HARE-benchmark.png
byline: by the KnowLab team
date: 2025-09-19
---
## The question

AI can now draft medical reports, but how do you tell whether a draft is clinically good? Standard text-similarity scores are a poor guide, and metrics designed for radiology do not suit histopathology, which has its own vocabulary of markers, anatomical sites and diagnoses.

## What we did

We built HARE, which stands for Histopathology Automated Report Evaluation. It has four parts: a dataset in which we labelled 813 de-identified clinical reports and 652 reports from The Cancer Genome Atlas, models that recognise the key entities and the relations between them, and a new score that compares the important findings in a reference report and a generated one. We also collected expert pathologists' ratings of generated reports to check the score against.

## What we found

Our entity-recognition and relation models, built on GatorTronS, reached the highest overall F1 score of 0.915 among those tested. The HARE score matched the experts better than conventional metrics such as ROUGE and METEOR, and better than radiology-based ones such as RadGraph-XL.

## Why it matters

Measuring what matters in a report is a precondition for making report-writing AI better. We are releasing the datasets, models and code for others to use.
