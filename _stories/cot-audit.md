---
layout: story
title: Better answers, shakier reasoning in small medical AI
summary: Small medical AI models trained to copy a larger model's reasoning get more answers right, but the steps they write out along the way contain more mistakes.
topics: [reliability, clinical-text]
paper_title: "Better Accuracies, Worse Reasoning: A Step-Level Audit of Medical Chain-of-Thought Distillation"
paper_url: https://arxiv.org/abs/2605.28301
authors: Jiang, Peng, Teng, Fu, Kim, Mi, Li and Wu
venue: EACL 2027, main conference
news: cot-audit
image: img/news/medical_cot_audit.png
audio: audio/cot-audit.mp3
audio_minutes: 2
byline: by the KnowLab team
date: 2026-11-14
---
## The question

Big AI models are expensive to run, so researchers often train a smaller one to imitate them. A popular recipe has the big model write out its reasoning, step by step, and the small model learns to produce the same kind of reasoning. This is called distillation.

It is usually judged by one thing only: does the small model get the final answer right? In medicine that is not enough. A doctor who reads an AI's explanation needs each step to be true, not only the last line.

## What we did

We trained a small model this way on medical exam style questions, then checked it twice. First we looked at its answers, as everyone does. Then we looked at its working, one step at a time, with an independent AI judge that was blind to writing style. A clinical expert also checked 150 of the steps without knowing which model wrote them.

## What we found

The answers got better. On a set of US medical licensing exam questions, accuracy rose from about 75% to about 84%, and the model's confidence matched its accuracy more closely.

The working got worse. The share of steps containing an error rose from about 31% to about 50%. The clinical expert saw the same pattern. It held across different judges, different teacher and student models, and other medical question sets.

Our reading is that the short answer format does little to keep the explanation honest. A capable small model learns to sound like an expert, with the right shape of reasoning, without reliably checking each claim along the way. The usual accuracy scores and measures of hedging did not show this shift.

## Why it matters

Distilled reasoning is now shared and reused widely. If a model's explanation is going to be read by a clinician, or used to train the next model, a good score on answers alone can hide shaky thinking. Step-level checks should be part of how these models are judged before anyone relies on their explanations.
