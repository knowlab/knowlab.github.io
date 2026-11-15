---
layout: story
title: "A reading list for machines: linking mental illness to light and sunlight"
summary: "The psycho-env corpus annotates 20 research articles on light, sunlight, bipolar disorder and depression, so text-mining tools can learn to find these links."
topics: [clinical-text]
areas: [mental-health]
paper_title: "The psycho-env corpus: research articles annotated for knowledge discovery on correlating mental diseases and environmental factors"
paper_url: https://ceur-ws.org/Vol-1891/paper6.pdf
authors: Wang et al.
venue: "KDH workshop at IJCAI 2017 (CEUR Workshop Proceedings 1891)"
news: psycho-env-corpus
byline: by the KnowLab team
date: 2017-08-20
---
## The question

Researchers use published studies to build knowledge about diseases, for example gene networks for disease gene discovery. For mental illness, the literature is far less used, which limits our understanding of how these conditions arise. It is known that environment shapes mental illness, but there is no complete list of which environmental factors matter for which condition.

## What we did

To help computers read this literature, we created the psycho-env corpus: published studies marked up by hand to show what each says about a mental illness and an environmental factor. Our first small version annotates 20 articles about two illnesses, bipolar disorder and depression, and two environmental factors, light and sunlight.

## What we found

The corpus exists as a first step and is shared openly on GitHub, together with its annotation guidelines and format. It is deliberately small, and the paper discusses what it leaves out, such as other environmental factors beyond light.

## Why it matters

Tools that mine the literature need examples to learn from. A carefully annotated set, even a small one, is the starting point for finding links between environment and mental illness at scale.
