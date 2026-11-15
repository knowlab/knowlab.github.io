---
layout: story
title: "Reading discharge letters to track anticoagulant use in atrial fibrillation"
summary: "An open-source language-processing pipeline calculated stroke and bleeding risk scores from 10,030 discharge summaries and showed rising anticoagulant use over seven years."
topics: [clinical-text]
areas: [cardiometabolic]
paper_title: "Semantic computational analysis of anticoagulation use in atrial fibrillation from real world data"
paper_url: https://doi.org/10.1371/journal.pone.0225625
authors: Bean et al.
venue: "PLoS ONE, 2019"
news: AF-Paper-Accepted
byline: by the KnowLab team
date: 2019-11-11
---
## The question

Atrial fibrillation is the most common abnormal heart rhythm and it raises the risk of stroke, which anticoagulant drugs control well. Studies of how often they are used have relied on registries, which are costly to collect and may not reflect real practice. Hospital records contain the answer, but in free text.

## What we did

We built an open-source pipeline that reads clinical text, finds the risk factors and calculates two standard scores: CHA2DS2-VASc, for the risk of ischaemic stroke, and HAS-BLED, for bleeding. We applied it to the discharge summaries of 10,030 patients with atrial fibrillation discharged between 2011 and 2017, and checked scores against two independent experts for 40 patients.

## What we found

The automatic CHA2DS2-VASc scores agreed strongly with the experts (average kappa 0.78, against 0.85 between the experts themselves). Agreement for HAS-BLED was lower (0.54, against 0.74). In high-risk patients, anticoagulant use rose significantly over the seven years, driven by the arrival of newer direct-acting drugs and by patients moving from antiplatelet drugs alone to anticoagulants.

## Why it matters

Risk scores can be computed from hospital text at scale, though the tools need further validation. And routine records can reproduce findings from large curated registries.
