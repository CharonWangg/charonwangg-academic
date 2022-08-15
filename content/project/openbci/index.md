---
title: Real-time Phase Locked Neural Feedback System Development
summary: A millisecond-level phase locked neural feedback system based on OpenBCI
tags:
  - Brain Computer Interface
  - Neural Feedback Control
  - Microcontroller
date: '2016-04-27T00:00:00Z'

# Optional external URL for project (replaces project detail page).
external_link: ''

image:
  caption: General System Overview
  focal_point: Smart

links:
  - icon: graduation-cap
    icon_pack: fas
    name: Publications
    url: https://dl.acm.org/doi/pdf/10.1145/3431943.3432284
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

The neural oscillation in electroencephalogram (EEG) signals is
highly related to people’s psychological cognitive ability. In this
work, an OpenBCI version of phase-locked feedback control system
has been implemented for real time alpha wave regulation. As
compared with the distributed system architecture on Brainamp,
PC and Arduino in the previous work, the new proposed system has
integrated all the modules for signal acquisition, phase estimation
and applying stimulation on one chip. Hence, the delay for signal
transmission can be effectively eliminated, which leads to a better
accuracy for phase estimation in phase-locked feedback control.
The results show the effective of the proposed system to alpha wave
regulation, which has significant modulation advantages in amplitude 
and frequency compared to Distributed BrainProduct Architectures.
![avatar](content/project/openbci/effect_1.png)
![avatar](content/project/openbci/effect_2.png)

Besides, we develop a PyQtGraph-based visualization tool for real-time 
monitoring on host computer, streaming data from OpenBCI board by Bluetooth 2.0
protocols. 
![avatar](content/project/openbci/visualization.png)

