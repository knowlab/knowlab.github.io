---
layout: story
title: "When expert doctors disagree, which labels should an AI learn from?"
summary: "Eleven intensive care consultants labelled the same patients differently, and the usual way of settling disagreements, a majority vote, gave worse AI models."
topics: [reliability]
paper_title: "The impact of inconsistent human annotations on AI driven clinical decision making"
paper_url: https://doi.org/10.1038/s41746-023-00773-3
authors: Sylolypavan et al.
venue: "npj Digital Medicine, 2023"
news: inconsistent-annotations-npj
image: img/news/npj-inconsistent-annotations.png
byline: by the KnowLab team
date: 2023-02-21
---
## The question

AI models for medicine learn from labels that clinical experts provide. But even highly experienced experts do not always label the same case the same way, because of personal judgement, bias and simple slips. The effect of this on real-world AI had been little studied.

## What we did

In an MSc project with us, real intensive care data was labelled by 11 ICU consultants. We then compared AI models trained on each consultant's labels and on different ways of combining them.

## What we found

There may not always be a single super expert in acute clinical settings. The standard way of reaching consensus, such as a majority vote, consistently led to suboptimal models. A better approach was to assess how learnable each set of labels is and to build the consensus only from the learnable ones, which gave the best models in most cases.

## Why it matters

If the labels behind a medical AI are inconsistent, the AI inherits the confusion. Checking label quality is as important as building the model.
