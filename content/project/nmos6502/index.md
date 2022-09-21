---
title: Could a Neural Network Understand Microprocessor
summary: Exploring causal relationships inside a large complex system with deep learning
tags:
  - Causality
  - Microcontroller
  - Deep Learning
date: '2016-04-27T00:00:00Z'

# Optional external URL for project (replaces project detail page).
external_link: ''

image:
  caption: Learning  causal discovery in a data-driven way
  focal_point: Smart

links:
  - icon: github
    icon_pack: fab
    name: Code
    url: https://github.com/CharonWangg/NMOS6502-Causality
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

Causal discovery (CD) from time-varying data is important in neuroscience, medicine, 
and machine learning. Techniques for CD include randomized experiments which are 
generally unbiased but expensive. It also includes algorithms like regression, 
matching, and Granger causality, which are only correct under strong assumptions 
made by human designers. However, as we found in other areas of machine learning, 
humans are usually not quite right and are usually outperformed by data-driven 
approaches. Here we test if we can improve causal discovery in a data-driven way. 
We take a system with a large number of causal components (transistors), the MOS 
6502 processor, and meta-learn the causal discovery procedure represented as a 
neural network. We find that this procedure far outperforms human-designed causal 
discovery procedures, such as Mutual Information and Granger Causality. We argue 
that the causality field should consider, where possible, a supervised approach, 
where CD procedures are learned from large datasets with known causal relations 
instead of being designed by a human specialist. Our findings promise a new approach 
toward CD in neural and medical data and for the broader machine learning community.


{{< figure src="projects/nmos6502/noise.png" caption="Methods comparison under different scales of noise" >}}


