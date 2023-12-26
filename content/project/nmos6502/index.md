---
title: Learning Causal Discovery
summary: Learn to discover causality inside a large complex system without human prior
tags:
  - Causal Discovery
  - Machine Learning
date: '2016-04-27T00:00:00Z'

# Optional external URL for project (replaces project detail page).
external_link: ''

image:
  size: actual
  caption: Learning  causal discovery in a data-driven way
  focal_point: Smart

links:
  - icon: github
    icon_pack: fab
    name: Code
    url: https://github.com/KordingLab/LearningCausalDiscovery
  - icon: graduation-cap
    icon_pack: fas
    name: Publications
    url: https://arxiv.org/abs/2209.05598
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

Causal discovery (CD) from time-varying data is important in neuroscience, medicine, and machine learning. 
Techniques for CD encompass randomized experiments, which are generally unbiased but expensive, and algorithms 
such as Granger causality, conditional- independence-based, structural-equation-based, and score-based methods 
that are only accurate under strong assumptions made by human designers. However, as demonstrated in other areas 
of machine learning, human expertise is often not entirely accurate and tends to be outperformed in domains with 
abundant data. In this study, we examine whether we can enhance domain-specific causal discovery for time series 
using a data-driven ap- proach. Our findings indicate that this procedure significantly outperforms human-designed, 
domain-agnostic causal discovery methods, such as Mutual Information, VAR-LiNGAM, and Granger Causality on the 
MOS 6502 microprocessor, the NetSim fMRI dataset, and the Dream3 gene dataset. We argue that, when feasible, 
the causality field should consider a supervised approach in which domain-specific CD procedures are learned from 
extensive datasets with known causal relationships, rather than being designed by human specialists. Our findings 
promise a new approach toward improving CD in neural and medical data and for the broader machine learning community.


{{< figure src="projects/nmos6502/table.png" caption="Methods comparison across different games and durations" >}}


