---
layout: story
title: "Telling types of stroke apart in UK Biobank by reading brain scan reports"
summary: "Combining language processing with clinical rules on brain scan reports identified bleeding strokes in UK Biobank with high accuracy, improving on coded data alone."
topics: [clinical-text, knowledge-graphs]
areas: [cardiometabolic, radiology]
paper_title: "Developing automated methods for disease subtyping in UK Biobank: an exemplar study on stroke"
paper_url: https://doi.org/10.1186/s12911-021-01556-0
authors: Rannikmae, Wu et al.
venue: "BMC Medical Informatics and Decision Making, 2021"
news: stroke-subtype-nlp
byline: by the KnowLab team
date: 2021-06-08
---
## The question

Large studies such as UK Biobank mostly find diseases through routinely collected codes, which are often incomplete and less accurate for specific subtypes. Stroke is a good example: it has several subtypes with different causes, so researchers need to tell them apart.

## What we did

From a sub-population of 17,249 Scottish UK Biobank participants, we identified those with a stroke code in hospital, death or primary care data and at least one brain scan report. We combined language processing of the scan reports with clinical knowledge, written as reusable rules, to work out the subtype: intracerebral haemorrhage, subarachnoid haemorrhage or ischaemic stroke.

## What we found

Of 225 participants with an incident stroke code, 207 had a usable scan report. Precision and recall for the individual findings ranged from 78 to 100%. At patient level the method was very good for intracerebral haemorrhage (89% for both), good for subarachnoid haemorrhage (82%) and lower for ischaemic stroke (73% precision, 64% recall), where coded data remain the better source.

## Why it matters

Used alongside coded data, automated reading of scan reports is a feasible and scalable way to improve disease subtyping. It was our first work combining NLP with reusable domain knowledge to derive sub-phenotypes.
