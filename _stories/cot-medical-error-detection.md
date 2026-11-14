---
layout: story
title: "Prompting a language model to find and fix mistakes in clinical notes"
summary: "Our entry to the MEDIQA-CORR 2024 shared task used step-by-step prompts to detect and correct medical errors, and placed in the top three for two of the three tasks."
topics: [reliability, clinical-text]
paper_title: "Chain-of-Though (CoT) prompting strategies for medical error detection and correction"
paper_url: https://arxiv.org/abs/2406.09103
authors: Wu et al.
venue: "NAACL 2024 Clinical NLP Workshop"
news: LLM-CoT-correct
image: img/news/cot-correction.png
byline: by the KnowLab team
date: 2024-06-13
---
## The question

Clinical notes can contain medical errors, and catching them automatically would help patient safety. The MEDIQA-CORR 2024 shared task set this as three sub-tasks: detect whether there is an error, find where it is, and correct it.

## What we did

We used a large language model with few-shot in-context learning, augmented with step-by-step reasoning prompts. In one method, we studied examples to design three reasoning prompts based on error types. In another, we used the training data to have the model work out why a note is correct or incorrect. We then combined the two with a rule-based ensemble.

## What we found

Across the three sub-tasks, the combined method ranked 3rd for sub-tasks 1 and 2 and 7th for sub-task 3 among all submissions.

## Why it matters

Careful prompting, with no retraining, can make a general model a useful clinical proofreader.
