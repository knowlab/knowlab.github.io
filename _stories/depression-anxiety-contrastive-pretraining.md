---
layout: story
title: "Predicting depression and anxiety in diabetes with limited primary care data"
summary: "We pre-trained a model on good-quality hospital records and fine-tuned it on primary care data, which predicted post-discharge depression and anxiety much better than baselines."
topics: [multimodal, clinical-text]
areas: [cardiometabolic, mental-health]
paper_title: "Applying contrastive pre-training for depression and anxiety risk prediction in type 2 diabetes patients based on heterogeneous electronic health records: a primary healthcare case study"
paper_url: https://doi.org/10.1093/jamia/ocad228
authors: Feng et al.
venue: "JAMIA, 2023"
news: jamia-depression-contrastive-learning
image: img/news/img-depression-contrastive-ehr.png
byline: by the KnowLab team
date: 2023-12-07
---
## The question

Primary care records in China are varied and limited, which makes it hard to assess the psychological risk of people with type 2 diabetes there. Hospitals hold better-quality data, but it is not the same setting.

## What we did

We built a deep learning framework called DAP. First we pre-trained a foundation model, using contrastive learning, a way for a model to learn patterns from unlabelled records, on good-quality records from 85,085 type 2 diabetes in-patients at a large university hospital. Then we fine-tuned it to predict depression using records from 149,596 patients on the Nanjing Health Information Platform.

## What we found

The approach was useful for predicting depression and anxiety after discharge among type 2 diabetes patients in primary care, with much higher performance than baseline models.

## Why it matters

Knowledge learnt in data-rich hospitals can be transferred to data-poor primary care, where most patients are seen.
