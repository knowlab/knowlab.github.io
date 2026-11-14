---
layout: story
title: "Teaching computers to spot falls, frailty and delirium in hospital discharge letters"
summary: "We built a hand-annotated collection of discharge summaries so that language models can learn to find geriatric syndromes in them."
topics: [clinical-text]
paper_title: "Geriatric Syndromes Extraction from Discharge Summaries: A New Dataset, Annotation Scheme and Initial Findings"
paper_url: https://www.frontiersin.org/journals/digital-health/articles/10.3389/fdgth.2026.1591050/
authors: Guellil et al.
venue: "Frontiers in Digital Health, 2026"
news: gs-data-IG
image: img/news/GS-IG-2026.png
byline: by the KnowLab team
date: 2026-06-10
---
## The question

Falls, dementia, delirium and malnutrition are among the geriatric syndromes that shape older people's lives and care. They cut across disease types and are poorly captured in the structured parts of health records, but are often described in the text of hospital discharge summaries. Teaching computers to find them needs examples that experts have labelled by hand, and good ones are scarce.

## What we did

We created a manually annotated collection of discharge summaries, with a labelling scheme for geriatric syndromes. We then tested several language models on it, both for deciding whether a document mentions a syndrome and for pinpointing where it is mentioned.

## What we found

The best models scored about 0.9 out of 1 on the document-level task. Frailty, falls and delirium were the easiest to find, while rarer syndromes and subtle context were harder. The pinpointing scores were measured on a simplified version of the annotations, so they are a baseline and not a ceiling.

## Why it matters

A shared, carefully labelled dataset gives researchers a common starting point for tools that help find older people at risk.
