---
layout: story
title: "Highlighting the key sentences in research papers to speed up curation"
summary: "NapEasy automatically highlights the sentences a curator needs in Parkinson's and Alzheimer's papers; in about 65% of cases the highlights were enough without reading the full text."
topics: [clinical-text]
paper_title: "Automated PDF highlighting to support faster curation of literature for Parkinson's and Alzheimer's disease"
paper_url: https://doi.org/10.1093/database/bax027
authors: Wu et al.
venue: "Database (Oxford), 2017"
news: Automated-PDF-highlighting
byline: by the KnowLab team
date: 2017-02-02
---
## The question

Parkinson's and Alzheimer's are the two most common neurodegenerative diseases and a huge global burden. Understanding them depends on knowledge that curators extract by hand from a vast literature. In the ApiNATOMY project, a curator would read each paper and mark the passages linking a test to brain anatomy. That is slow and costly.

## What we did

We built NapEasy, a tool that automatically highlights the relevant sentences in a paper's PDF. This is related to summarising a paper, but harder, because the number of sentences to highlight varies a lot from paper to paper.

## What we found

On a corrected test set, the tool reached a macro-averaged F1 of 0.51, which we saw as a promising first step. In a user evaluation, the highlights significantly helped curation in most cases, and in about 65% of cases the highlights were enough to do the curation task without reading the full text.

## Why it matters

Pre-digesting papers for curators means faster processing and lower cost. The code is open on GitHub.
