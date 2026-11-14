---
layout: story
title: "Teaching clinical knowledge to language models through how they split words"
summary: "K-Tokeniser builds medical concepts such as drugs and diseases into the way a language model reads text, so it needs less training data."
topics: [clinical-text, knowledge-graphs]
paper_title: "Infusing clinical knowledge into language models by subword optimisation and embedding initialisation"
paper_url: https://doi.org/10.1016/j.compbiomed.2025.110747
authors: Hasan et al.
venue: "Computers in Biology and Medicine, 2025"
news: ktokenizer
image: img/news/tokenizer-2025.png
byline: by the KnowLab team
date: 2025-08-08
---
## The question

Language models read text by chopping words into pieces called tokens. For everyday English that works well. For clinical text, long drug and disease names often get split into meaningless fragments, which makes it harder for models to learn their meaning.

## What we did

We built K-Tokeniser. It uses medical concepts from resources such as the UMLS, or from a specific task's text, to choose better tokens at training and at use. For the new tokens, it sets up their starting representation in a way that avoids having to pre-train the language model from scratch.

## What we found

For automated clinical coding, a model built with K-Tokeniser improved the Micro F1 score (a standard accuracy measure) by 13%. It beat the clinicalBERT baseline using only half the training data for extracting medical concepts and less than a fifth of it for coding.

## Why it matters

Labelled clinical data is expensive. Building domain knowledge into the model's reading process gets better results from far less of it.
