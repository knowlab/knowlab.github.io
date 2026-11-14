---
layout: story
title: "Using language models to improve a traceable rare-disease diagnosis tool"
summary: "Combining a language model with an ontology-based ranking tool improves rare-disease diagnosis while keeping the evidence trail."
topics: [knowledge-graphs, clinical-text]
paper_title: "Learning to Fuse LLMs with Ontology Rankers for Rare-Disease Diagnosis"
paper_url: https://arxiv.org/abs/2609.02473
authors: Jiang et al.
venue: "arXiv preprint, 2026"
news: rd-llm-fusion
image: img/news/rd_llm_fusing.png
byline: by the KnowLab team
date: 2026-09-02
---
## The question

Ontology-based tools for rare disease match a patient's features against known disease profiles, so every suggestion can be traced back to the features that support it. Language models can also suggest diagnoses from the same description, but without a clear evidence trail. Rather than choosing one over the other, can the language model make the tool better without giving up its evidence?

## What we did

We built a model that looks at both ranked lists, how much they agree, and the ontology support behind each candidate, and learns for each case how far to trust each side. Before comparing, we removed a known source of test leakage, caused by benchmark cases and ontology records coming from the same publications.

## What we found

Across eight open language models, fusion raised the top-choice accuracy of the ontology tool by about 8 percentage points on one dataset and about 20 points on another. With a different model reached through an online service and without retraining, accuracy rose from 0.1657 to 0.2176. For 90.8% of correct fused diagnoses, the disease still had candidate-level evidence that can be inspected.

## Why it matters

Language models can strengthen an established diagnostic tool without throwing away the structured evidence that makes it trustworthy.
