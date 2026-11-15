---
layout: story
title: "Letting AI see where the radiologist looks on a chest X-ray"
summary: "Overlaying a radiologist’s eye-gaze heatmap on the X-ray improved the accuracy of vision-language models across several chest X-ray tasks."
topics: [multimodal, reliability]
areas: [radiology]
paper_title: "Enhancing Human-Computer Interaction in Chest X-ray Analysis using Vision and Language Model with Eye Gaze Patterns"
paper_url: https://arxiv.org/abs/2404.02370
authors: Kim et al.
venue: "arXiv preprint, 2024 (accepted at MICCAI 2024)"
news: xray-eye-gaze
image: img/news/xray-eye-gaze.png
byline: by the KnowLab team
date: 2024-04-03
---
## The question

Computer-aided diagnosis for chest X-rays has become good, but the conversation between the AI and the radiologist is usually one-way, with the radiologist only supplying the image. What if the AI also knew where the radiologist was looking?

## What we did

We recorded eye-gaze data from radiologists and turned it into heatmaps that we overlaid on the X-ray, highlighting the areas of intense focus. We gave these, together with text prompts, to vision-language models and tested four tasks: visual question answering, report automation, error detection and differential diagnosis.

## What we found

Adding eye gaze significantly improved the accuracy of the analysis. Fine-tuning with gaze also outperformed other medical vision-language models on every task except visual question answering.

## Why it matters

A radiologist's attention is expert knowledge that the AI can learn from. This points to a more human-centred way of building diagnostic AI. It is the starting point for the later Look & Mark work.
