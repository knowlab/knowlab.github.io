---
layout: story
title: "Can AI that sees X-rays catch mistakes in radiology reports?"
summary: "We tested multimodal language models on spotting errors in chest X-ray reports by checking them against the radiograph."
topics: [multimodal, reliability]
paper_title: "Exploring Multimodal Large Language Models for Radiology Report Error-checking"
paper_url: https://arxiv.org/abs/2312.13103
authors: Wu et al.
venue: "arXiv preprint, 2023"
news: multimodal-llm-radiology-errors
image: img/news/mllm.png
byline: by the KnowLab team
date: 2023-12-20
---
## The question

Generative AI and foundation models are moving fast. In radiology, one practical question is whether they could be good assistants for spotting mistakes in reports by cross-checking them against the X-ray.

## What we did

We created 1,000 reports with synthetic errors from two real-world chest X-ray datasets. We then set two kinds of tasks: a yes-or-no question, whether there is an error, and a multi-way question, what type of error it is. Multimodal language models were tested on both.

## What we found
Among publicly available models, LLaVA v1.5 did best at the yes-or-no check. Instruction tuning, which means training it on examples of this task, improved it by 47.4% on MIMIC-CXR and 25.4% on IU X-ray, and it surpassed the domain expert's accuracy on MIMIC-CXR by 1.67%. Where a clinician got a case wrong in a small test set, the ensemble of models picked up 71.4% of those. All the models did poorly at naming the type of error, so that harder task remains open.

## Why it matters

Reports with errors can delay or misdirect care. An AI second reader that checks the words against the image could be a useful safety net, which is why we kept developing this line of work.
