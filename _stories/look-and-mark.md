---
layout: story
title: "Teaching AI to read chest X-rays by following where radiologists look"
summary: "Giving a multimodal model the places radiologists look and the regions they mark improves the reports it writes, without retraining it."
topics: [multimodal, reliability]
paper_title: "Look & Mark: Leveraging Radiologist Eye Fixations and Bounding boxes in Multimodal Large Language Models for Chest X-ray Report Generation"
paper_url: https://aclanthology.org/2025.findings-acl.909/
authors: Kim et al.
venue: "Findings of ACL, 2025"
news: look_mark
image: img/news/landm.png
featured: true
byline: by the KnowLab team
date: 2025-05-28
---
## The question

AI models that write radiology reports from X-rays can invent findings. Radiologists have knowledge the model lacks, such as where they look first and what they mark as important. Can we pass that expertise to the model?

## What we did

We introduced Look & Mark. Look uses the points where a radiologist fixed their gaze, and Mark uses boxes drawn around regions of interest. Both are given to the model as guidance, through in-context learning, so the models do not need extensive retraining.

## What we found

Reports became more clinically relevant, with fewer hallucinations. The gains were largest on clinical measures. A domain-specific model, CXR-LLaVA, improved by 1.2% overall, while LLaVA-Med improved by 9.2%. A general-purpose model, LLaVA-OV, reached an 87.3% clinical average, the highest of all models tested, even above models trained specifically for chest X-ray reports.

## Why it matters

Human expertise, added in a light-touch way, can make general AI models safer and more useful for reading medical images.
