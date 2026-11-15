---
layout: story
title: "An AI proofreader for radiology reports"
summary: "A three-stage method that detects, locates and corrects mistakes in radiology reports, using medical knowledge to help language models do it."
topics: [clinical-text, knowledge-graphs]
areas: [radiology]
paper_title: "Error Correction in Radiology Reports: A Knowledge Distillation-Based Multi-Stage Framework"
paper_url: https://doi.org/10.1609/aaai.v40i46.41295
authors: Wu et al.
venue: "AAAI 2026 (AI for Social Impact track)"
news: RadCorrection-AAAI2026
image: img/news/RadCorrAAAI2026.png
audio: audio/radiology-report-error-correction.mp3
audio_minutes: 1
featured: true
byline: by the KnowLab team
date: 2026-01-20
---
## The question

Radiologists are busy, and mistakes inevitably slip into their reports. Speech recognition mishears words, terms are ambiguous and templates cause inconsistencies. Such errors can delay treatment and sometimes harm patients. General language models are not yet good at catching them.

## What we did

We gave language models medical expertise in two ways. One is distilling a medical knowledge graph, and the other is looking up outside reference knowledge. We also split the proofreading into three stages, detection, localisation and correction, much as an expert radiologist would review a report. To test it fairly we built a benchmark of real radiology reports with realistic errors, validated by practising radiologists.

## What we found

Across several language models, error detection accuracy improved by up to 31.56% and processing time fell by 37.4%. Radiologists who reviewed the results judged them better in clinical relevance and factual consistency than existing approaches.

## Why it matters

Better report quality with less effort from radiologists, which should particularly help places with fewer resources.
