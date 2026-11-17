---
layout: story
title: "Breaking complex data into layers of concepts, from raw signals to syndromes"
summary: "A sparse autoencoder that splits raw data into a background layer, basic building blocks and the combinations of them that form recognisable concepts, which helps find rare signals and generate realistic synthetic data."
topics: [knowledge-graphs, reliability]
paper_title: "HH-SAE: Discovering and Steering Hierarchical Knowledge of Complex Manifolds"
paper_url: https://arxiv.org/abs/2605.10536
authors: Wu et al.
venue: "arXiv preprint, 2026"
news: HH-SAE
audio: audio/hh-sae.mp3
audio_minutes: 1
byline: by the KnowLab team
date: 2026-05-11
---
## The question

Raw data does not come with concepts attached. A patient record is a long list of lab values, vital signs and codes, and a scan is a grid of pixels. An important concept, such as diabetes in a record or pneumonia in a chest scan, is rarely one signal. It is built from many smaller signals that only mean something in combination, and the dense, common background around them tends to drown them out. Tools that look inside AI models usually spend their capacity on that background, so the rare, meaningful features stay hidden. We call this feature density conflict.

## What we did

We built the Hybrid Hierarchical sparse autoencoder, or HH-SAE. A sparse autoencoder breaks a model's internal representation into separate, interpretable features. HH-SAE arranges them in three layers. A contextual layer absorbs the common background and sets it aside. An atomic layer finds the basic building blocks in what is left. A compository layer finds the combinations of atoms, or motifs, that act like recognisable concepts.

Because knowledge is laid out in layers, it can be used in two ways. It can pick out diseases and events, for classification and prediction. And it can generate synthetic data by switching on chosen motifs, so the data follows a discovered mechanism instead of only copying statistics.

## What we found

In hospital records, the method split a broad group of patients labelled as diabetic into three distinct physiological patterns: kidney and electrolyte failure, a stable chronic group, and unstable blood sugar. It also recovered 45 patients whom simpler models missed. They looked quiet on paper, but several small signals were firing together before any single marker reached a clinical alert level.

The same idea carried over to a different field. Without retraining, it reached an AUC of 0.92 in fraud detection. Removing the background-subtraction step cost about 13% of its usefulness, which shows that step matters. When we used the discovered motifs to steer the generation of synthetic data, performance (AUPRC) was 9.9% better than with leading generative methods.

## Why it matters

If knowledge can be laid out in layers, we can see which concepts a model has found, and use them to detect rare events earlier and to build training data that follows a mechanism rather than only the statistics. This is a preprint and has not been peer reviewed. The results come from hospital records and fraud data, and the motifs it finds still need checking by domain experts.
