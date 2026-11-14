---
layout: story
title: "Not one sepsis but several: splitting patients by organ failure helps prediction"
summary: "Grouping ICU patients by their pattern of organ dysfunction improved sepsis prediction across three machine-learning models, especially in specificity."
topics: [reliability]
paper_title: "On classifying sepsis heterogeneity in the ICU: insight using machine learning"
paper_url: https://doi.org/10.1093/jamia/ocz211
authors: Ibrahim et al.
venue: "Journal of the American Medical Informatics Association, 2020"
news: jamia-icu
byline: by the KnowLab team
date: 2020-01-17
---
## The question

Spotting sepsis early is vital for patient outcomes. Machine-learning models try to recognise it from health records, but sepsis is not one condition: patients differ in which organs fail and how. Ignoring that may be why results have been mixed.

## What we did

Using 13,728 intensive care records from the public MIMIC-III database, we identified sepsis subpopulations with clearly different patterns of organ dysfunction. We then picked, for each group, the measurements that matter most, and used these as background knowledge in classification experiments with random forests, gradient boosting and support vector machines to tell patients who develop sepsis in the ICU from those who do not.

## What we found

Features chosen using the subpopulations performed better whichever model was used. The gain was especially clear in specificity, which is a current bottleneck for sepsis prediction.

## Why it matters

Accounting for the different faces of a disease can steer machine learning towards more personalised models for complex conditions such as sepsis.
