---
layout: story
title: "Mining tumour test results from thousands of research abstracts with AI"
summary: "IHC-LLMiner uses a language model to find and extract tumour staining profiles from PubMed abstracts, faster and more accurately than GPT-4o on this task."
topics: [clinical-text]
paper_title: "IHC-LLMiner: Automated extraction of tumour immunohistochemical profiles from PubMed abstracts using large language models"
paper_url: https://arxiv.org/abs/2504.00748
authors: Kim et al.
venue: "arXiv preprint, 2025"
news: IHC-LLMiner
image: img/news/ihc-llminer.png
byline: by the KnowLab team
date: 2025-04-01
---
## The question

Pathologists use a lab test called immunohistochemistry, or IHC, to help work out what kind of tumour they are looking at. Which stains show up in which tumours is written across a huge number of research papers, but gathering it by hand is slow.

## What we did

We built IHC-LLMiner, a pipeline with two jobs. First it decides which PubMed abstracts are relevant. Then it pulls out the tumour and staining details from the relevant ones. We fine-tuned a language model called Gemma-2 for the task and mapped the results onto standard medical concepts so they can be compared consistently.

## What we found

The fine-tuned model got the relevance decision right 91.5% of the time and extracted the profiles correctly 63.3% of the time. It beat GPT-4o on both accuracy and speed.

## Why it matters

This points to a way of turning scattered literature into organised, searchable data that researchers and clinicians can use at scale.
