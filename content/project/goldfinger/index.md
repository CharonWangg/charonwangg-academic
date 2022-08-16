---
title: Gold Finger
summary: Finger flexion angles prediction from ECoG by machine learning
tags:
  - Neural Decoding
  - Brain-Computer Interface
  - Machine Learning
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
    url: https://github.com/CharonWangg/521-Goldfinger
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
In this project, to better predict finger flexion for individual subjects, we developed an 
algorithm called logistic-weighted random forest, which utilized the
classification results from logistic regression as a weight, and then combines the
nonlinear regression results from random forest to generate a final data glove
prediction. LASSO was incorporated in the logistic regression to allow variable
selection and regularization. The addition of random forest is necessary in that it
can provide non-linear prediction results required by the problem, while avoid
overfitting commonly occurred in polynomial regression. The entire algorithm
includes data pre-processing, feature extraction, feature processing, model
training, prediction, cross-validation, and post-processing. This pipeline 
achieved 52.8% and 46.7% correlation on the public leaderboard and private leaderboard, 
listed as Top 5 solution in the 2020 BE521 Brain-Computer Interface Final Competition.

{{< figure src="projects/goldfinger/effect.png" caption="Algorithm prediction visualization" theme="dark" >}}
