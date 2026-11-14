---
layout: story
title: "Predicting who will deteriorate in hospital, even when it is rare"
summary: "A two-part model learns what the first 24 hours of a patient looks like before a bad outcome and predicts mortality and ICU admission with PR-AUCs around 0.9."
topics: [reliability, multimodal]
paper_title: "A Knowledge Distillation Ensemble Framework for Predicting Short- and Long-term Hospitalisation Outcomes from Electronic Health Records Data"
paper_url: https://doi.org/10.1109/JBHI.2021.3089287
authors: Ibrahim, Bean et al.
venue: "IEEE Journal of Biomedical and Health Informatics, 2022"
news: Knowledge-Distillation
byline: by the KnowLab team
date: 2021-06-15
---
## The question

Predicting which patients will deteriorate supports timely decisions, resource planning and personalised care. But bad outcomes are infrequent, and most prediction models struggle to catch the rare positive cases.

## What we did

In work led by Zina Ibrahim at King's College London, we built a scalable framework that uses vital signs and laboratory results from the first 24 hours after admission. It stacks two parts. The first is an unsupervised model that learns a representation of the time series and separates the uncommon patterns that end in an adverse event from the common ones that do not. The second is a gradient boosting model that refines the prediction using static information such as demographics, admission details and clinical summaries. It also gives visual justifications for its predictions.

## What we found

In three case studies, covering intensive care and general ward settings, the model outperformed existing platforms, with average PR-AUCs (a score suited to rare outcomes, where 1 is perfect) of 0.891 for mortality and 0.908 for ICU admission and readmission.

## Why it matters

Handling rare outcomes well, with explanations attached, is what makes this kind of prediction useful at the bedside.
