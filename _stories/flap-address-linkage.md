---
layout: story
title: "Matching messy typed addresses to the right property"
summary: "FLAP links free-text addresses to the UK's official property database with 99.2% adjusted accuracy and is released as open-source software."
topics: [clinical-text]
paper_title: "FLAP: a framework for linking free-text addresses to the Ordnance Survey Unique Property Reference Number database"
paper_url: https://doi.org/10.3389/fdgth.2023.1186208
authors: Zhang et al.
venue: "Frontiers in Digital Health, 2023"
news: flap-address-hz
byline: by the KnowLab team
date: 2023-10-26
---
## The question

Health and social care records hold addresses typed as free text, with typos, abbreviations and local shorthand. To study care-home residents, housing moves or the geography of care, they must be matched to the official property record (the UPRN).

## What we did

FLAP pairs a machine-learning classifier, which judges whether a typed address and an official record match, with a fuzzy alignment step that copes with typos and reordered words. We tested it on the addresses of 771,588 people in NHS Tayside and NHS Fife.

## What we found

Adjusted matching accuracy was 0.992 on a test set of 3,876 addresses. It coped with typos, alternative formats and partly wrong information, and lets users set a confidence threshold or return the top candidates.

## Why it matters

Open, validated tools for address linkage open the door to geographic health research. The code is on GitHub.
