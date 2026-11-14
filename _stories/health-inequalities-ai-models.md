---
layout: story
title: "Measuring whether an AI model makes health inequalities worse"
summary: "A generic framework quantifies inequality in data and AI models as the area between two curves, and found significant inequalities in real intensive care data and models."
topics: [reliability]
paper_title: "Quantifying Health Inequalities Induced by Data and AI Models"
paper_url: https://doi.org/10.24963/ijcai.2022/721
authors: Wu, Sylolypavan, Wang and Wild
venue: "IJCAI-ECAI 2022 (AI for Good track)"
news: DA-AUC-IJCAI2022
image: img/news/DAindex-news.png
byline: by the KnowLab team
date: 2022-05-02
---
## The question

Without a good way to detect and mitigate inequalities caused by AI, AI may do more harm than good in healthcare and widen the gaps that already exist. Practitioners lacked a technical tool to quantify these inequalities so they could debug and audit their data and models.

## What we did

We proposed a generic allocation-deterioration framework. Inequality is quantified as the area between two curves that relate the score a model allocates to patients to how much those patients deteriorate. We tested it on ten synthetic datasets (more than 33,000 patients) made from a real intensive care dataset, HiRID, and then on two real ICU datasets and AI models trained for two resource allocation scenarios.

## What we found

The framework detected and quantified inequality in proportion to the amount we built in. Compared with men, women had up to 33% poorer deterioration in markers of prognosis in HiRID ICUs. All four AI models assessed induced significant inequalities (2.45% to 43.2%) for non-White compared with White patients, and the models significantly worsened inequalities already in the data in 3 of 8 assessments, one by more than nine times.

## Why it matters

Bias in the data is only part of the picture, because models can add to it. This gave us a way to measure both, and it led to our later funded work on quantifying and mitigating bias in medical AI. The code is open.
