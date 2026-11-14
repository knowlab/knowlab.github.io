---
layout: story
title: "SemEHR: turning weeks of hospital record searching into minutes"
summary: "SemEHR is an open-source tool that finds what clinical notes say about patients, cutting recruitment-criteria checking from days to minutes."
topics: [clinical-text, knowledge-graphs]
paper_title: "SemEHR: A general-purpose semantic search system to surface semantic data from clinical notes for tailored care, trial recruitment, and clinical research"
paper_url: https://doi.org/10.1093/jamia/ocx160
authors: Wu et al.
venue: "Journal of the American Medical Informatics Association, 2018"
news: semehr-jamia
byline: by the KnowLab team
date: 2018-02-10
---
## The question

Much of what a hospital knows about a patient is locked in free-text notes: nursing records, radiology reports and discharge summaries. Getting at it for research, to run a hospital or to find patients for a trial usually needs a bespoke tool built for each study, which is slow and expensive.

## What we did

We built SemEHR, an open-source search and analysis system for health records. It finds mentions of a wide range of medical concepts in notes, with their context (for example, whether the condition is present or ruled out), and assembles them into a timeline for each patient. Users search it through an ontology, a structured medical vocabulary, so ordinary extraction tasks become search queries.

## What we found

SemEHR has been used in several UK hospitals. In two studies on the Clinical Record Interactive Search system, it reached F-measures of 93% for hepatitis C and 99% for HIV when identifying the right patients. At King's College Hospital it supports recruitment into the 100,000 Genomes Project, and checking recruitment criteria dropped from days to minutes. Vital signs it extracted from intensive care notes were about 97% accurate.

## Why it matters

Work that took weeks or months can sometimes be done in hours or minutes, with a more complete view of each patient than study-specific tools give. The code is open on GitHub.
