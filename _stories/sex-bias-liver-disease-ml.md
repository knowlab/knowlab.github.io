---
layout: story
title: "Do liver disease prediction models miss more women?"
summary: "Models built from a widely used liver disease dataset had a higher false-negative rate for women, which would mean more missed diagnoses."
topics: [reliability]
paper_title: "Investigating for bias in healthcare algorithms: a sex-stratified analysis of supervised machine learning models in liver disease prediction"
paper_url: https://doi.org/10.1136/bmjhci-2021-100457
authors: Straw and Wu
venue: "BMJ Health & Care Informatics, 2022"
news: bias-healthcare-algorithms
image: img/news/bias-news.png
byline: by the KnowLab team
date: 2022-04-26
---
## The question

The Indian Liver Patient Dataset is used extensively to build algorithms that predict liver disease. Given known differences between the sexes in how liver disease is diagnosed and managed, these algorithms need scrutiny for bias.

## What we did

In work led by Isabel Straw, we reviewed the published studies on this dataset, recreated the reported models (random forests, support vector machines, Gaussian Naive Bayes and logistic regression), and examined them by sex. We defined four experiments: training on sex-unbalanced or balanced data, with and without feature selection.

## What we found

We reproduced published accuracies above 70% and found a previously unobserved performance gap. Across all classifiers, women had a higher false-negative rate. The two models reported as the most effective, random forest and logistic regression, showed the largest gap.

## Why it matters

In practice a higher false-negative rate means more missed diagnoses for women and a lack of appropriate care. Checking for bias early can reveal inequalities in current practice, and stops them being built into algorithms.
