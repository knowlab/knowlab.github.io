---
layout: story
title: "Hand-written rules or machine learning for reading brain scan reports?"
summary: "On Scottish stroke imaging reports, a hand-crafted system was the most accurate, but machine learning was a feasible alternative when no one has time to write rules."
topics: [clinical-text]
paper_title: "Named Entity Recognition for Electronic Health Records: A Comparison of Rule-based and Machine Learning Approaches"
paper_url: https://arxiv.org/abs/1903.03985
authors: Gorinski et al.
venue: "HealTAC (Healthcare Text Analytics Conference), 2019"
news: NER-comparision
byline: by the KnowLab team
date: 2019-03-01
---
## The question

To find diseases, symptoms and body locations in free-text records, a system has to do named entity recognition. You can write rules by hand, or train a model. Which approach is better on clinical text, and what does each cost?

## What we did

We compared three kinds of system for brain imaging reports, with a focus on stroke: a rule-based one, a deep learning one and a transfer learning one. We trained on a common dataset and tested on Scottish radiology reports from two sources, the Edinburgh Stroke Study data from NHS Lothian and reports from NHS Tayside.

## What we found

A hand-crafted system was the most accurate way to label the records automatically. But machine learning approaches can be a feasible alternative where there are no resources to build a manual system.

## Why it matters

Hand-written rules cost expert time. This comparison helps teams choose between that cost and a slightly less accurate model. It also fed into the later EdIE-R tool comparison work.
