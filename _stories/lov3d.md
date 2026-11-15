---
layout: story
title: "Teaching an AI to read brain scans over time and show its working"
summary: "LoV3D reads a patient’s brain MRI scans over time, measures regions step by step, and only then gives a diagnosis, which cuts down on made-up conclusions."
topics: [multimodal, reliability]
areas: [radiology]
paper_title: "LoV3D: Grounding Cognitive Prognosis Reasoning in Longitudinal 3D Brain MRI via Regional Volume Assessments"
paper_url: https://arxiv.org/abs/2603.12071
authors: Jiang et al.
venue: "arXiv preprint, 2026"
news: lov3d
image: img/news/lov3d.png
byline: by the KnowLab team
date: 2026-03-12
---
## The question

Brain scans taken over time can show how a disease such as Alzheimer's is progressing. Today's AI tools split this job up. Some give only a label, some give measurements nobody has interpreted, and AI that writes text can sound fluent while inventing conclusions.

## What we did

LoV3D follows the steps a careful reader would. It reads the scan, assesses each brain region, compares with the patient's earlier scan, and only then gives a diagnosis of normal, mild cognitive impairment or dementia, with a written summary. Each step has to be consistent with the last. To train it, an automatic checker scores the model's answers against standard reference measurements, so no human labelling was needed.

## What we found

On a held-out test of 479 scans from 258 people, the three-way diagnosis was right 93.7% of the time. It also worked on new data from other sites without retraining, scoring 95.4% on one collection and 82.9% on another.

## Why it matters

A diagnosis that comes with its working can be checked. Grounding each step in measurable evidence is a way to make imaging AI less likely to hallucinate.
