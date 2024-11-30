---
title: 'Causal-Copilot: An Autonomous Causal Analysis Agent'
summary: A toolkit that integrates LLM capabilities and domain expertise to enable automated causal analysis for scientific researchers and data scientists.
tags:
  - Causal Analysis
  - Machine Learning
  - Artificial Intelligence
  - Large Language Models
date: '2024-11-29T00:00:00Z'

# Optional external URL for project (replaces project detail page).
external_link: ''

image:
  size: actual
  caption: Autonomous Causal Analysis with Causal-Copilot
  focal_point: Smart

links:
  - icon: github
    icon_pack: fab
    name: Code
    url: https://github.com/Lancelot39/Causal-Copilot
  - icon: rocket
    icon_pack: fas
    name: Demo
    url: https://huggingface.co/spaces/Causal-Copilot/Causal-Copilot
  - icon: youtube
    icon_pack: fab
    name: Video
    url: https://www.youtube.com/watch?v=A6j80I97Slg

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

Understanding causal relationships is fundamental to scientific discovery, enabling researchers to move beyond mere correlation and establish the underlying mechanisms that drive natural and social phenomena. Recent years have witnessed significant theoretical advancements in causal discovery, yielding a diverse array of sophisticated methodologies. However, the complexity of these methods—each with its distinct assumptions, applicability conditions, and technical nuances—has created substantial barriers for scientists outside the field of causal analysis, often deterring them from adopting these powerful analytical tools in their research.

Causal-Copilot is a LLM-oriented toolkit for **automatic causal analysis** that uniquely integrates domain knowledge from large language models with established expertise from causal discovery researchers. Designed for scientific researchers and data scientists, it facilitates the identification, analysis, and interpretation of causal relationships within real-world datasets through natural dialogue. The system autonomously orchestrates the entire analytical pipeline-analyzing statistics, selecting optimal causal analysis algorithms, configuring appropriate hyperparameters, synthesizing executable code, conducting uncertainty quantification, and generating comprehensive PDF reports—while requiring minimal expertise in causal methods. This seamless integration of conversational interaction and rigorous methodology culminates enables researchers across disciplines to focus on domain-specific insights rather than technical implementation details.


### Features

- **Automated Algorithm Selection**: Automatically selects the most suitable causal analysis algorithms and hyperparameters.
- **LLM-Enhanced Post Processing**: Includes uncertainty quantification, graph pruning, and direction refinement using LLM insights.
- **User-Friendly Interface**: Enables interaction through natural dialogue and visualizes results with intuitive graphs and figures.
- **Comprehensive Reporting**: Generates detailed PDF reports with analysis workflows, visualizations, and interpretations.
- **Extensibility**: Open for integrating new causal discovery methods and tools.

### Performance on Simulated Data

Causal-Copilot achieves state-of-the-art performance on simulated datasets, outperforming traditional methods like the PC algorithm:

| Metric    | Baseline | Causal-Copilot |
|-----------|----------|----------------|
| Precision | 78.6%    | **81.6%**      |
| Recall    | 78.2%    | **81.0%**      |
| F1-score  | 76.1%    | **79.3%**      |

### Online Demo

🚀 Interactive demo on [Hugging Face Space](https://huggingface.co/spaces/Causal-Copilot/Causal-Copilot).

---

{{< figure src="projects/copilot/workflow.png" caption="Architecture of Causal-Copilot" >}}

