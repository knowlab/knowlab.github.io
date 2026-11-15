---
layout: story
title: "Showing AI not just where a radiologist looked, but in what order"
summary: "Turning a radiologist's eye movements into a short video helped general-purpose vision-language models write better chest X-ray reports and diagnoses, in one case beating specialist medical models."
topics: [multimodal, reliability]
areas: [radiology]
paper_title: "RadEyeVideo: Enhancing general-domain Large Vision Language Model for chest X-ray analysis with video representations of eye gaze"
paper_url: https://arxiv.org/abs/2507.09097
authors: Kim, Wu and Wu
venue: "arXiv preprint, 2025"
news: radeyevideo
image: img/news/xray-eye-gaze.png
byline: by the KnowLab team
date: 2025-07-15
---
## The question

Earlier work, including ours, gave AI models a radiologist's eye gaze as a heatmap or as text. Both show where the radiologist looked, but not the order. Yet radiologists tend to read an X-ray in a structured sequence, and that order carries expertise.

## What we did

We built RadEyeVideo, which turns the eye-fixation data into a video sequence capturing both where and when the radiologist looked. We tested it on chest X-ray report generation and disease diagnosis with three general-purpose, open-source vision-language models that can take video input. We also built a pipeline that produced eye-gaze videos for 2,298 chest X-rays from MIMIC-CXR, and compared the video approach against heatmap and text prompts.

## What we found

With eye-gaze videos, performance improved by up to 24.6% in report generation, and by 15.2% on average across both tasks. One general-domain model, LLaVA-OneVision, went on to beat specialist medical models such as MAIRA-2 and CheXagent, which were trained on large amounts of chest X-ray data.

## Why it matters

An expert's way of looking is knowledge that can be passed to an AI without retraining it on huge medical datasets. Because of data policy, only the code and protocols are shared, so others can rebuild the pipeline.
