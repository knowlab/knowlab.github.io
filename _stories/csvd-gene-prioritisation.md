---
layout: story
title: "Which algorithm best finds new genes for small vessel disease of the brain?"
summary: "We benchmarked seven network-based gene-ranking methods for cerebral small vessel disease and found one clearly best overall, with an important limit on discovering truly new genes."
topics: [knowledge-graphs]
paper_title: "Benchmarking network-based gene prioritization methods for cerebral small vessel disease"
paper_url: https://doi.org/10.1093/bib/bbab006
authors: Zhang et al.
venue: "Briefings in Bioinformatics, 2021"
news: network-benchmarking-bib
byline: by the KnowLab team
date: 2021-01-04
---
## The question

Network-based algorithms rank genes by how closely they connect to genes already known to cause a disease, using networks of protein interactions and gene-disease links. It is not obvious which algorithm is best for a specific disease. We looked at cerebral small vessel disease, a cause of stroke and dementia.

## What we did

We curated protein-gene interactions and gene-disease associations from databases, built the networks, and benchmarked seven representative algorithms, using known disease genes as seeds. We tested them with leave-one-out cross-validation and with an external check against the MEGASTROKE genome-wide association study.

## What we found

A method called random walk with restart, which spreads a signal outwards from known disease genes through the network, performed best overall. A known disease gene held back as a test typically came back at about rank 186 out of 19,463 genes, although it is prone to bias from well-connected genes. Another algorithm, GenePanda, had the most genes later confirmed by GWAS in its top 200. Pure network methods are unlikely to find novel genes that are not linked to known ones.

## Why it matters

The choice of algorithm should be made before applying one to a specific disease. We released the tools so the benchmark can be repeated for other diseases.
