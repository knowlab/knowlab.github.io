---
layout: story
title: "Four NLP tools, one brain-scan task: don't expect them to work out of the box"
summary: "Comparing four off-the-shelf tools on brain radiology reports showed that performance varies widely, so tools need checking and adapting before clinical use."
topics: [clinical-text, reliability]
paper_title: "Understanding the performance and reliability of NLP tools: a comparison of four NLP tools predicting stroke phenotypes in radiology reports"
paper_url: https://doi.org/10.3389/fdgth.2023.1184919
authors: Casey et al.
venue: "Frontiers in Digital Health, 2023"
news: nlp-comparision-AC
byline: by the KnowLab team
date: 2023-09-28
---
## The question

Natural language processing could read radiology reports automatically, but is it reliable enough for real clinical use when tools are taken from one setting to another?

## What we did

We compared four off-the-shelf rule-based and neural tools (EdIE-R, ALARM+, ESPRESSO and Sem-EHR) on three findings in brain reports: ischaemic stroke, small vessel disease and atrophy. We used two cohorts, one from NHS Fife and one from Generation Scotland, and compared tool output with clinical experts and with readings of the scan images.

## What we found

EdIE-R scored highest for ischaemic stroke in both cohorts (an F1 score, which balances missed and false findings, of at least 93%), followed by ALARM+. Against the scan reads, however, ALARM+ scored 80% and EdIE-R 66% for stroke. Scores differed across tools, phenotypes and cohorts.

## Why it matters

Tools cannot simply be used out of the box. Knowing the context a tool was built in is essential to judge whether it fits, or needs retraining.
