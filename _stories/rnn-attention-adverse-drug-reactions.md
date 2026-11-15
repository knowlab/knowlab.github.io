---
layout: story
title: "Teaching a neural network to spot side effects in clinical text"
summary: "Adding custom word embeddings and an attention mechanism to a bidirectional LSTM network for extracting adverse drug reactions from health-record text."
topics: [clinical-text]
paper_title: "Improving RNN with Attention and Embedding for Adverse Drug Reactions"
paper_url: https://doi.org/10.1145/3079452.3079501
authors: Pandey et al.
venue: "Digital Health (DH '17), ACM, 2017"
news: rnn-attention-adr
byline: by the KnowLab team
date: 2017-07-02
---
## The question

The free-text notes in health records describe patients in rich detail, including the side effects they have from medicines. A computer has to find those mentions and work out how they relate to the drug involved before the information can be used for research. Clinical writing is full of abbreviations and rare terms, which general-purpose language tools handle poorly.

## What we did

We built a neural network that reads text in both directions, a bidirectional LSTM, and made two changes to it. First, we gave it word embeddings (numerical representations of words) learned from clinical text, including drug names, diseases, side-effect terms and uncommon abbreviations. Second, we added an attention mechanism, which lets the network learn which words in a sentence matter most when labelling each word.

## What we found

This was a short paper and a first look at how far these two additions help in picking out adverse drug reactions in clinical text. Later work by other groups on adverse drug event extraction cites it.

## Why it matters

Side effects are often recorded only in free text. Better extraction from notes is what lets researchers study them at scale, which we then did in our ADEPt pipeline and later studies.
