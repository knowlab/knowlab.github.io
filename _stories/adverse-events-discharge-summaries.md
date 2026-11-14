---
layout: story
title: "Finding adverse events in the discharge letters of older patients"
summary: "A hand-labelled collection of discharge summaries from older patients, covering 14 adverse events such as falls and delirium, shows where language models still struggle."
topics: [clinical-text]
paper_title: "Adverse Event Extraction from Discharge Summaries: A New Dataset, Annotation Scheme, and Initial Findings"
paper_url: https://arxiv.org/abs/2506.14900
authors: Guellil et al.
venue: "ACL 2025 (main conference)"
news: ade-acl
byline: by the KnowLab team
date: 2025-06-17
---
## The question

Older patients are often left out of the datasets used to teach computers to read clinical text, yet they are the ones most likely to have things go wrong in hospital. Discharge summaries describe these events, but in free text that is hard for software to read.

## What we did

We built a manually annotated collection of discharge summaries from elderly patients. It covers 14 clinically significant adverse events, such as falls, delirium and bleeding inside the skull, along with details like whether the event was negated and whether it happened in hospital. The labelling scheme can handle mentions that are split up or overlap, which is rare in earlier work. We then tested several language models.

## What we found

Models did well at the broad document-level question of which events a letter mentions, with the best score of 0.943 out of 1. They did much worse at pinpointing fine detail, with a score of 0.675, especially for rare events and complex attributes.

## Why it matters

High overall scores can hide real gaps. The dataset, available on request through DataLoch, gives others a benchmark for improving how well computers detect underrepresented events and nuanced clinical language.
