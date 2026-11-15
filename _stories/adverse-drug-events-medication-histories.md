---
layout: story
title: "Predicting drug side effects from a patient's whole medication history"
summary: "Encoding overlapping medication episodes over time predicted three side effects of psychiatric drugs with 93% accuracy, about 10% better than treating medication as static."
topics: [knowledge-graphs]
areas: [mental-health]
paper_title: "Encoding Medication Episodes for Adverse Drug Event Prediction"
paper_url: https://www.research.ed.ac.uk/en/publications/encoding-medication-episodes-for-adverse-drug-event-prediction/
authors: Wu et al.
venue: "SGAI AI-2016 (Springer); preliminary version at the IJCAI 2016 healthcare data workshop"
news: adr-medication-episodes
byline: by the KnowLab team
date: 2016-12-13
---
## The question

Side effects of medicines, known as adverse drug reactions, can be serious and cost health services a lot. Understanding what leads to them could make drug treatment more effective and tailored to the individual. But in long-term illnesses, a patient is often on several drugs at once, started and stopped at different times, so it is hard to tell which combination at which moment is behind a side effect. Hospital records hold this history, but it is rarely used.

## What we did

We found a way to turn a patient's overlapping medication episodes into a compact record of what they were taking at any given time. We then enriched it with a drug ontology, a structured vocabulary that groups related drugs, and with basic patient details, and used it to predict whether a side effect would occur. We tested it on records from the South London and Maudsley NHS Foundation Trust, the largest mental health provider in Europe.

## What we found

Using the profiles of 38,000 mental health patients, we identified 240,000 mentions of dry mouth, constipation and enuresis (bedwetting), plus 44,000 mentions where the patient did not have them. The approach reached 93% prediction accuracy and F-measure. In an earlier workshop version of the work, the encoding improved accuracy by 10% compared with treating medication as a fixed list.

## Why it matters

Doctors rarely get a warning that a patient's particular drug history makes a side effect likely. Capturing the timeline of medication is a first step towards that, and it fed into our later work on predicting unknown side effects.
