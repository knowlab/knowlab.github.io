---
layout: story
title: "Combining seven COVID-19 risk models so the best one is used for each patient"
summary: "An ensemble that picks the most competent models for each patient beat every individual model across four cohorts in the UK and China."
topics: [reliability]
paper_title: "Ensemble learning for poor prognosis predictions: a case study on SARS-CoV-2"
paper_url: https://doi.org/10.1093/jamia/ocaa295
authors: Wu et al.
venue: "JAMIA, 2020"
news: covid-ensemble-jamia
byline: by the KnowLab team
date: 2020-11-11
---
## The question

A risk model built from one group of patients rarely performs well everywhere, and the COVID-19 pandemic exposed this clearly. Could we get a more robust model by combining models from different places?

## What we did

We re-implemented seven published COVID-19 prediction models that came from diverse cohorts and used different techniques. We then built an ensemble framework that, for each individual patient, leans on the models best suited to that patient. We tested all models on four international cohorts, two from the UK and two from China, with 5,394 patients in total.

## What we found

Individual models did well on some cohorts and badly on others, and all of them did better on the Chinese cohorts. The ensemble was consistently best at separating high- from low-risk patients, at predicting accurate risks, and in clinical usefulness.

## Why it matters

When models are learnt from complementary populations, combining them can deliver the strengths of all of them. The code is open on GitHub.
