---
layout: story
title: "Reusing a language-processing model without starting from scratch"
summary: "A phenotype-embedding approach shows where an existing model will work on new records and where it won't, saving around 80% of the effort of blind adaptation."
topics: [clinical-text, reliability]
paper_title: "Efficient Reuse of Natural Language Processing Models for Phenotype-Mention Identification in Free-text Electronic Medical Records: A Phenotype Embedding Approach"
paper_url: https://doi.org/10.2196/14782
authors: Wu et al.
venue: "JMIR Medical Informatics, 2019"
news: NLP-Transfer-Learning-Accepted
byline: by the KnowLab team
date: 2019-10-22
---
## The question

Building a language-processing model for clinical text takes effort, so reusing one built elsewhere is attractive. But in a new setting, with new data or new conditions to find, you normally have to keep validating and retraining it to see whether it works. That is slow and often wasteful.

## What we did

We framed the problem of adapting a model to a new task and identified two sources of waste, "duplicate waste" and "imbalance waste", that get in the way. Our fix is a phenotype embedding, a way of making the language patterns of an old setting and a new one visible and comparable, without needing labelled data from the new setting. We tested it on a large mental health registry, reusing models in four tasks for identifying phenotype mentions, meaning mentions of a condition or trait relating to a person.

## What we found

The approach modelled language patterns well and could guide which model to reuse. It also showed which novel language patterns need validation and retraining in the new task, saving around 80% of the effort that "blind" adaptation requires.

## Why it matters

Clinical NLP will only spread if reusing tools is cheap. Knowing where a model will fail is the key.
