---
title: Shallow Mind
summary: A Pytorch-lightning based Deep Learning framework for personal usage
tags:
  - Deep Learning
date: '2016-04-27T00:00:00Z'

# Optional external URL for project (replaces project detail page).
external_link: ''

image:
  caption: Algorithm flow chart
  focal_point: Smart

links:
  - icon: github
    icon_pack: fab
    name: Code
    url: https://github.com/CharonWangg/shallowmind
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
Inspired by MMSegmentation, I want all of my Deep Learning projects to be
simplified to a single 'config.py', and do not need to worried about training 
except for specific model/dataset. So I decide to make a highly disentangled 
one based on Pytorch-lightning.

Now support:
  * Custom Model Class
    * Architecture, 
    * Backbone, 
      * Embedding layers like Base/Linear/Convolutional
      * LSTM/Transformer/TCN/Timm_models/NeuralPredictors
    * Head like MLP, Poolers,
  * Custom Dataset Class
    * Single dataset and Multiple datasets concatenation
    * Pipeline for augmentations from Albumentations, Tsaug, etc
  * Various Optimizers and Schedulers 
    * Warmup like Linear, Cosine
    * Optimizers like Adam, AdamW, SGD, etc
    * Schedulers like OneCycleLR, CosineAnnealingLR, etc
  * Various Loss and Metrics
    * Multi loss fusion like CrossEntropy, BCE, FocalLoss, etc
  * Logging and Checkpointing
  * Distributed Training
  * Simple api train/infer for use

All you need is to write a config.py/model class/dataset class and run it :)
