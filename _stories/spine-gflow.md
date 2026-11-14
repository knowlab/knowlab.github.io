---
layout: story
title: "Teaching a spine-MRI model without hand-drawn outlines"
summary: "Spine-GFlow segments vertebrae, discs and the spinal canal in lumbar MRI without any manual annotation, matching a fully supervised model (Dice 0.914 vs 0.916)."
topics: [multimodal]
paper_title: "Spine-GFlow: A hybrid learning framework for robust multi-tissue segmentation in lumbar MRI without manual annotation"
paper_url: https://doi.org/10.1016/j.compmedimag.2022.102091
authors: Kuang et al.
venue: "Computerized Medical Imaging and Graphics, 2022"
news: spine-gflow
image: img/news/spin-gflow.png
byline: by the KnowLab team
date: 2022-06-16
---
## The question

Most MRI segmentation models learn from outlines drawn by hand. That is tedious, and more so when several structures must be outlined on every scan.

## What we did

Spine-GFlow combines what a neural network learns from the image with anatomical prior knowledge. A rule-based method first produces rough seed areas automatically, a proposal step blends multi-scale image features with anatomy, and a training loss refines pixel classification. No manual annotation is used. We tested it on two independent datasets, one with images from three different scanners.

## What we found

Without any manual labels, segmentation of vertebral bodies, discs and the spinal canal was comparable to a fully supervised model (mean Dice score, a measure of overlap with the expert outline where 1 is perfect: 0.914 vs 0.916), and it held up across scanner settings.

## Why it matters

Removing the annotation bottleneck makes it far easier to build spine-imaging tools for new hospitals and scanners.
