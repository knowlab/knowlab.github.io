---
layout: story
title: "A unified view of how deep learning assigns medical codes"
summary: "A survey that breaks automated medical coding models into four building blocks so the field can be understood and compared."
topics: [clinical-text]
paper_title: "A Unified Review of Deep Learning for Automated Medical Coding"
paper_url: https://doi.org/10.1145/3664615
authors: Ji et al.
venue: "ACM Computing Surveys, 2024"
news: survey-automated-coding
image: img/news/acm-surveys-coding.png
byline: by the KnowLab team
date: 2024-05-21
---
## The question

Hospitals assign standard codes to describe what happened to each patient, which is essential for running health services. Deep learning can predict these codes from clinical documents, but the many published models are hard to compare because they are designed in different ways.

## What we did

We proposed a unified framework that splits medical coding models into four components: encoders that extract features from the text, mechanisms for building deep encoder designs, decoders that turn the internal representation into codes, and the use of auxiliary information. We summarised recent advanced models within this framework, and described the benchmarks, real-world use and open challenges.

## What we found

The framework gives a general understanding of the building blocks of medical coding models and a way to relate new work to previous work.

## Why it matters

A common map helps newcomers get started and helps researchers see which ideas are really new.
