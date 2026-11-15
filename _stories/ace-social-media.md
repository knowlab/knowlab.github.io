---
layout: story
title: "Finding traces of difficult childhoods in social media, with ontologies to guide the AI"
summary: "An ontology-guided, self-supervised method for spotting adverse childhood experiences in social media posts, producing a public resource for further research."
topics: [clinical-text]
areas: [mental-health]
paper_title: "Ontology-Driven Self-Supervision for Adverse Childhood Experiences Identification Using Social Media Datasets"
paper_url: https://doi.org/10.5220/0011531100003523
authors: Wu, Smith and Wu
venue: "Workshop on Scarce Data in AI for Healthcare, 2022"
news: ace-social-media
image: img/news/JW-ace.png
byline: by the KnowLab team
date: 2023-03-20
---
## The question

Adverse childhood experiences, meaning highly stressful and potentially traumatic events in childhood or adolescence, are linked to higher risks of mental illness and other problems later in life. Studying them at scale needs a lot of text to learn from, but labelled examples are scarce.

## What we did

We built an ontology-driven, self-supervised approach. It takes the output of basic language processing and learns compact numerical representations of the concepts with an auto-encoder, a neural network that learns by compressing and rebuilding its input, guided by a structured vocabulary of the concepts involved. The aim was a publicly available resource built from social media text.

## What we found

The method produces a resource that can support large-scale machine learning, such as training modern language models, on social media data, without relying on large amounts of hand labelling.

## Why it matters

Scarce labelled data is a common obstacle in health research. Using domain knowledge to supervise the AI is one way around it. The paper and code are openly available.
