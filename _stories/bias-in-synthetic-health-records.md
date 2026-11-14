---
layout: story
title: "When AI writes fake patient records, whose bias does it copy?"
summary: "Larger language models wrote more complete synthetic health records, but also showed stronger gender and racial bias."
topics: [reliability, clinical-text]
paper_title: "Evaluation and Bias Analysis of Large Language Models in Generating Synthetic Electronic Health Records: Comparative Study"
paper_url: https://www.jmir.org/2025/1/e65317/
authors: Huang et al.
venue: "Journal of Medical Internet Research, 2025"
news: llm-bias
image: img/news/llm-bias.png
byline: by the KnowLab team
date: 2025-05-12
---
## The question

Language models can write synthetic health records, realistic but invented patient notes that could be used to train or test systems without exposing real patients. But if the models carry hidden biases, the synthetic records will too.

## What we did

We compared several language models on how well they generate health records and then looked at how the gender and racial make-up of the generated patients differed across diseases.

## What we found

Larger models such as Yi-34B, Qwen-14B and Llama 2 13B wrote more comprehensive records, but their gender and racial biases grew as well, a trade-off between performance and bias. Bias showed up in all the models, not just the large ones. Gender bias closely followed real-world disease rates, while racial bias appeared only for some diseases, with some over-representing White or Black patients and under-representing Hispanic and Asian groups.

## Why it matters

Better synthetic data should not come at the cost of fairness. These results show the need for methods that reduce bias and for benchmarks that test for it.
