---
layout: story
title: "Three ways to teach AI to curate a chemistry ontology, compared"
summary: "For building a biomedical ontology, we compared in-context learning, fine-tuning and supervised learning on more than 1.8 million facts."
topics: [knowledge-graphs, reliability]
paper_title: "Benchmarking and Analyzing In-context Learning, Fine-tuning and Supervised Learning for Biomedical Knowledge Curation: a focused study on chemical entities of biological interest"
paper_url: https://arxiv.org/abs/2312.12989
authors: Groves et al.
venue: "arXiv preprint, 2023"
news: benchmarking-nlp-paradigms-chebi
image: img/news/benchmarking-chebi.png
byline: by the KnowLab team
date: 2023-12-20
---
## The question

Curating a biomedical ontology, the structured vocabulary that organises knowledge in a field, is slow manual work. We had the task of automating it for ChEBI, the Chemical Entities of Biological Interest ontology, and asked which AI approach works best.

## What we did

We compared three ways of using language models: in-context learning, where the model is shown examples in the prompt, fine-tuning, and supervised learning. We broke the main question into four specific ones. The experiments covered three GPT models, including GPT-4, one domain-specific model, PubMedBERT, and six embedding models, across 15 set-ups and more than 1.8 million facts.

## What we found
There was no single winner. Shown examples in the prompt, GPT-4 reached accuracies of 0.916, 0.766 and 0.874 on the three curation tasks. But a conventional supervised model trained on about 260,000 facts beat it on accuracy on all three. The fine-tuned PubMedBERT matched the best supervised models on two tasks and fell behind on the third. With less data, or more lopsided data, the supervised and fine-tuned models got worse, and GPT-4 came out ahead on two of the tasks when fewer than 6,000 facts were available.

## Why it matters
Language models given good prompts can be useful curation assistants, but they do not make the older approaches obsolete. When you have plenty of task-specific data, training your own model still wins. When you have little, prompting GPT-4 is the better bet. Knowing which suits which situation saves effort for anyone maintaining a knowledge base.
