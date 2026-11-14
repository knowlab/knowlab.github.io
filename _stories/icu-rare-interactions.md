---
layout: story
title: "Finding the rare patterns in ICU data that signal trouble"
summary: "A framework that spots rare, meaningful interactions between patient measurements in intensive care and uses them to predict outcomes such as sepsis, while explaining why."
topics: [reliability, multimodal]
paper_title: "Modeling Rare Interactions in Time Series Data Through Qualitative Change: Application to Outcome Prediction in Intensive Care Units"
paper_url: https://arxiv.org/abs/2004.01431
authors: Ibrahim, Wu and Dobson
venue: "ECAI 2020"
news: ECAI
byline: by the KnowLab team
date: 2020-02-21
---
## The question

Intensive care units record patients continuously, sometimes every few seconds. Yet outcomes are often decided by a small number of rare interactions between measurements, and those interactions are defined less by exact values than by how far readings drift from normal over time. Most prediction models cannot explain themselves.

## What we did

We built a framework that describes the data in qualitative terms such as "rising" or "low", links events through a graph of their temporal relations, and then searches for the interaction patterns most likely to produce a given outcome. The patterns found are then used as features for prediction.

## What we found

In experiments on sepsis prediction with real ICU data, the discovered patterns were meaningful in medical terms, and using them as features gave better prediction. Unlike most approaches, the framework can also explain the outcomes it predicts.

## Why it matters

Explainable patterns of deviation from normal are easier for clinicians to check and trust than a bare risk score.
