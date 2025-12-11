---
title: Turtle Soup Generator
summary: An interactive situation puzzle game system 
tags:
  - Story Generation
  - Natural Language Processing
  - Deep Learning
date: '2016-04-27T00:00:00Z'

# Optional external URL for project (replaces project detail page).
external_link: ''

image:
  caption: Situation puzzle generation workflow
  focal_point: Smart

links:
  - icon: github
    icon_pack: fab
    name: Code
    url: https://github.com/CharonWangg/Turtle_Soup_Generator
  - icon: file-pdf
    icon_pack: fas
    name: Report
    url: https://drive.google.com/file/d/19T_KACaioy4uNIs9o2PG14J1_zq_J5W8/view?usp=sharing
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
Situation puzzle is a popular text-based interactive game. In
such a game, there is a moderator and a player, or a group
of players. The moderator has a complete story in mind and
provides the player(s) with the beginning and the ending of
a story; the player(s), on the other hand, are expected to
figure out the step-by-step details of story development by
asking the moderator ”yes-or-no” questions about the story.
The game would end either when the player(s) figure out
the complete story line or when a preset number of ques-
tions are asked before complete the story. The challenging
and intriguing part of this game is that the player(s) need to
come up with a story with only the beginning and the ending
while also make sure the logical relations in the story align
with commonsense.

We propose to build a system (TurtleSoup) that not only
automatically generate high-quality story for a situation puz-
zle game but also handles the job of the moderator to in-
teract with player(s). With minimum human intervention,
TurtleSoup is capable of providing comprehensive interac-
tive experience that can be entertaining.

{{< figure src="projects/turtle_soup/generation.png" caption="Generation and Question Answering demo" >}}
