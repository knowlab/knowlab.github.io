---
layout: story
title: "Finding drug side effects hidden in psychiatric clinical notes"
summary: "ADEPt, a rule-based pipeline built with clinicians and pharmacists, found 19 side effects of antipsychotics and antidepressants in free-text records, with an average F-measure of 0.83."
topics: [clinical-text]
areas: [mental-health]
paper_title: "ADEPt, a semantically-enriched pipeline for extracting adverse drug events from free-text electronic health records"
paper_url: https://doi.org/10.1371/journal.pone.0187121
authors: Iqbal et al.
venue: "PLoS ONE, 2017"
news: ADEPt
byline: by the KnowLab team
date: 2017-01-01
---
## The question

Adverse drug events, the unintended harms of treatment, hit patients' quality of life and burden health services. Hospital records document them, but mostly as free-text notes that software cannot read easily. In a note, a side effect may be something that happened long ago, something that might happen, or something being discussed in general, and each of those means something different.

## What we did

We built ADEPt, a rule-based pipeline, and tested it on records of 264,000 patients from four UK psychiatric hospitals. It tells apart whether a mention is historical or current, whether it is asserted, hypothetical, retrospective or general discussion, and cases where the status is only implied by the surrounding text. We wrote the rules by hand, with clinicians and pharmacists, after studying how side effects appear in different kinds of notes.

## What we found

Across 19 side effects of antipsychotic and antidepressant drugs, the average F-measure (a combined accuracy score, where 1 is perfect) and accuracy were both 0.83. ADEPt also improved on ConText, a widely used method for reading the context around a mention.

## Why it matters

Side effects of psychiatric drugs are poorly captured in coded data. Reading the notes gives researchers a way to study them at scale.
