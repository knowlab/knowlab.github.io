---
layout: story
title: "Spotting tiny lesions in eye scans for diabetic retinopathy"
summary: "RMCA U-net is a neural network that outlines hard exudates in retinal photos more accurately than standard networks."
topics: [multimodal]
areas: [cardiometabolic, radiology]
paper_title: "RMCA U-net: Hard exudates segmentation for retinal fundus images"
paper_url: https://doi.org/10.1016/j.eswa.2023.120987
authors: Fu et al.
venue: "Expert Systems with Applications, 2023"
news: RMCA
image: img/news/RMCA-UNET.png
byline: by the KnowLab team
date: 2023-07-23
---
## The question

Hard exudates, small bright deposits in the retina, are a key sign used to grade diabetic retinopathy. They take up little of the image, have irregular shapes and low contrast, so they are easily confused with other structures such as the optic disc, and automatic outlining is hard.

## What we did

We designed a neural network called RMCA U-net. It uses a U-shaped design with residual connections to capture subtle features, plus a module that fuses information at multiple scales and an improved channel attention module to find small, sparse lesions. We trained and tested it on three datasets.

## What we found

RMCA U-net beat the other convolutional networks we compared with. Against a standard U-net it improved PR-mAP by 6% on one public dataset, recall by 10% on another, and F1 score by 20% on a local dataset.

## Why it matters

More accurate lesion outlining supports more reliable grading of diabetic retinopathy from eye images.
