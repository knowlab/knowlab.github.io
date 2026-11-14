---
layout: story
title: "A chest X-ray assistant that learns from where the radiologist looks"
summary: "Eye-fixation prompts improved a multimodal model for chest X-ray diagnosis, and fine-tuning with only 658 reports beat a model trained on 17,000."
topics: [multimodal, reliability]
paper_title: "Human-in-the-Loop Chest X-Ray Diagnosis: Enhancing Large Multimodal Models with Eye Fixation Inputs"
paper_url: https://doi.org/10.1007/978-3-031-67751-9_6
authors: Kim et al.
venue: "Workshop on Trustworthy AI for Healthcare, 2024"
news: Human-in-the-Loop-X-Ray
image: img/news/hmitl-x-ray.png
byline: by the KnowLab team
date: 2024-08-03
---
## The question

Today's interaction with medical AI assistants is mostly limited to sending an image and a text prompt. Radiologists have attention patterns, where they look and for how long, that carry expertise. Can an assistant use those?

## What we did

We proposed a human-in-the-loop approach in which eye-fixation prompts, recording the location and duration of a radiologist's attention, are given to a large language-and-vision assistant. The assistant interacts with the radiologist in two ways: recommending possible diagnoses and confirming the diagnosis in a report.

## What we found

The eye-fixation prompts significantly improved accuracy for differential diagnosis and report confirmation. Fine-tuning LLaVA-1.5 with only 658 reports that include fixation information beat the previous state-of-the-art model, LLaVA-ERR, which was trained on 17,000 reports, by 5%.

## Why it matters

The interaction works both ways, since the model benefits from the radiologist's expertise while supporting their decisions.
