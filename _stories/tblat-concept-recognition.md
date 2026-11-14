---
layout: story
title: "Reading messy clinical text with a tool inspired by DNA sequence search"
summary: "TBLAT borrows ideas from BLAST, the tool for searching DNA sequences, to match misspelt and abbreviated clinical terms to the right concepts."
topics: [clinical-text, knowledge-graphs]
paper_title: "Term-BLAST-Like Alignment Tool for Concept Recognition in Noisy Clinical Texts"
paper_url: https://doi.org/10.1093/bioinformatics/btad716
authors: Groza et al.
venue: "Bioinformatics, 2023"
news: concept-recognition
image: img/news/blast-concept.png
byline: by the KnowLab team
date: 2023-11-23
---
## The question

Health record text is full of spelling mistakes, abbreviations and non-standard ways of writing clinical concepts. Matching such text to standard medical concepts is hard for tools that expect clean input.

## What we did

We built the Term-BLAST-like alignment tool, TBLAT, inspired by the BLAST algorithm that biologists use to search DNA sequences. It screens text for likely matches by counting short fragments, then scores the candidates by how well they fit typical spelling-error patterns learnt from 2.9 million clinical notes. We compared it with five widely used tools.

## What we found

TBLAT increased recall by 10% on scientific publications and 20% on health records compared with the next best method. It can be used on its own or to complement existing tools.

## Why it matters

Linking messy text to standard concepts is a first step for almost everything else we do with clinical language, so better matching helps everything downstream.
