---
title: Could a Neural Network Understand Microprocessor
summary: Exploring causal relationships inside a large complex system with deep learning
tags:
  - Causal Discovery
  - Microcontroller
  - Deep Learning
date: '2016-04-27T00:00:00Z'

# Optional external URL for project (replaces project detail page).
external_link: ''

image:
  caption: Cause effect on the NMOS6502 when running Donkey Kong
  focal_point: Smart

links:
  - icon: github
    icon_pack: fab
    name: Code
    url: https://github.com/CharonWangg/NMOS6502-Causality
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

Causal inference (CI) from time-varying data is important in neuroscience, medicine, and machine
learning. Techniques for CI include randomized experiments which are generally unbiased but
expensive. It also includes algorithms like regression, matching, and Granger causality, which are
only correct under very strong assumptions made by human designers. However, as we found
in other areas of machine learning, human designers are usually not quite right and are usually
outperformed by data driven approaches. Here we thus take a system with a large number of
causal components (transistors), the NMOS 6502 processor, and meta-learn the causal inference
procedure. We find that this procedure far outperforms human designed inference procedures,
like raw correlations, mutual information, or Granger causality. We argue that causal inference
should consider, where possible, a supervised approach, where CI procedures are learned on large
temporal datasets with known causal relations. This promises a new approach towards CI in neural
and medical data and for the broader machine learning community.

{{< figure src="projects/nmos6502/regular_methods.png" caption="ausal inference method comparison in the pairwise transistor relationship classification" >}}


