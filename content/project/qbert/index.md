---
title: QBert
summary: Query Embeddings using Contrastive Learning without Negative Samples
tags:
  - Semantic Search
  - Self-supervised Learning
  - Natural Language Processing
  - Deep Learning
date: '2016-04-27T00:00:00Z'

# Optional external URL for project (replaces project detail page).
external_link: ''

image:
  caption: Query embeddings training framework
  focal_point: Smart

links:
  - icon: github
    icon_pack: fab
    name: Code
    url: https://github.com/Vopaaz/QBert
url_code: ''
url_pdf: ''
url_slides: ''
url_video: ''

# Slides (optional).
#   Associate this project with Markdown slides.
#   Simply enter your slide deck's filename without extension.
#   E.g. `slides = "example-slides"` references `content/slides/example-slides.md`.
#   Otherwise, set `slides = ""`.
slides: ""
---

Semantic search is an essential topic in Natural Language Processing
(NLP). Mainstream methods to conduct it are to adopt the same general
large sentence encoder to acquire representations of queries and candidates
and calculate their similarity. However, such methods are still suboptimal
as they ignore the different characteristics of query and candidate corpus.
To this end, we propose Query-BERT, a query embedding specific encoder
to provide high-quality query embedding in a light model way. Inspired
by the success of self-supervised learning (SSL) in computer vision, we
leverage BYOL, a mature image contrastive learning approach without
the need for negative samples, onto query embedding training to acquire
a more robust query representation. Experiments show that under appro-
priate augmentation, our SSL method can reach competitive performance
to the supervised method on Quora question duplicated pairs without big
batch size and negative samples. However, the alignment between Query-
BERT and candidates embedding is not satisfied and demands further
optimization. We hope that this success of transfer learning could moti-
vate people to rethink the appropriate effectiveness utilization of the light
model and the role of domain-specific learning in the machine learning
problem
