---
layout: story
title: "Letting a pathology AI learn new things without forgetting the old, and without keeping patient images"
summary: "Generative latent replay plus attention-based regularisation reduced catastrophic forgetting in a histology image task without storing past examples."
topics: [reliability, multimodal]
paper_title: "Attentive Latent Replay for Continual Learning in Pathology"
paper_url: https://doi.org/10.1109/ISBI60581.2025.10980701
authors: Patra et al.
venue: "IEEE ISBI, 2025"
news: latent-replay-pathology
byline: by the KnowLab team
date: 2025-05-12
---
## The question

Pathology datasets arrive over time and bring new classes of data, so a model must keep learning. But when a model is trained on new tasks it tends to forget old ones, which is known as catastrophic forgetting. Privacy, legal and storage limits often make it impossible to keep the old images to retrain on.

## What we did

We proposed a replay method built on generative models: instead of storing past images, the model replays generated latent representations of earlier tasks. We added a knowledge-regularisation step that uses attention embeddings from earlier tasks, so the model keeps track of which spatial features mattered most.

## What we found

Combining attention-based regularisation with generative latent replay gave better continual-learning performance in non-stationary data settings, shown on a representative histology image analysis task.

## Why it matters

Clinical AI will not be trained once and frozen. Learning from new data without hoarding patient images is a step towards models that can be updated safely over time.
