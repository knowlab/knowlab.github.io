---
layout: story
title: "Do medical vision-language AI models make things up? A benchmark"
summary: "We built a benchmark of medical images with question-answer sets to test how often AI models hallucinate, and which prompting strategies help."
topics: [reliability, multimodal]
paper_title: "Hallucination Benchmark in Medical Visual Question Answering"
paper_url: https://arxiv.org/abs/2401.05827
authors: Wu, Kim and Wu
venue: "arXiv preprint, 2024 (tiny paper at ICLR 2024)"
news: Hallucination-Benchmark
image: img/news/hallucination_performance.png
byline: by the KnowLab team
date: 2024-01-11
---
## The question

Large AI models that look at pictures and answer questions about them could make useful visual assistants in health care. But they can hallucinate, which means giving confident answers that are not supported by the image. That had not been tested thoroughly in clinical settings.

## What we did

We created a hallucination benchmark of medical images paired with question-and-answer sets, and used it to evaluate the state-of-the-art models in depth.

## What we found
We named the benchmark HALT-MedVQA. It tests models with fake or nonsensical questions and with questions paired with an unrelated image, among other scenarios. LLaVA v1.5 variants did best, and the 7B version even beat the medical LLaVA-Med models. Training on medical data did not guarantee fewer hallucinations: LLaVA-Med did worse than the general model it was built from. The paper also compares prompting strategies, which can reduce the problem. The dataset and code are on GitHub (knowlab/halt-medvqa).

## Why it matters

Before such assistants are trusted in clinics, we need to measure how often they make things up. A benchmark gives everyone a common way to check.
