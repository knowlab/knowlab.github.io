---
layout: story
title: "Predicting drug side effects that clinical trials missed"
summary: "A knowledge-graph method predicted unknown adverse drug reactions (AUC 0.92 on known ones), and high-confidence predictions were checked against real hospital records."
topics: [knowledge-graphs]
paper_title: "Knowledge graph prediction of unknown adverse drug reactions and validation in electronic health records"
paper_url: https://doi.org/10.1038/s41598-017-16674-x
authors: Bean et al.
venue: "Scientific Reports, 2017"
news: kg-adr
byline: by the KnowLab team
date: 2017-11-27
---
## The question

Adverse drug reactions cost the NHS an estimated £466 million a year in hospital admissions. Clinical trials can only reveal some of them, so a drug on the market may have side effects nobody knows about yet. Can we predict them before enough patients have been harmed to notice?

## What we did

We built a knowledge graph, a network linking drugs, their protein targets, their uses and their known side effects. An unknown side effect appears as a missing link, so the task is to predict the missing links. We then checked the predictions against anonymised electronic health records from the South London and Maudsley NHS Foundation Trust, rather than relying on spontaneous reports, which are known to be under-reported.

## What we found

The method classified known causes of adverse reactions very well (AUC 0.92, where 1 is perfect). When 10% of the known links were hidden, it recovered 68% of them on average. High-confidence predictions were confirmed in the health records significantly more often than chance, and it outperformed standard methods such as logistic regression, decision trees and support vector machines.

## Why it matters

Predicting reactions that trials did not observe could improve patient safety. The method is general, so it could also be applied to other questions, such as finding new uses for old drugs.
