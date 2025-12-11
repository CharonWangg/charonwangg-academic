---
title: 'Causal-Copilot: An Autonomous Causal Analysis Agent'
summary: An LLM-powered autonomous agent that automates the entire causal analysis pipeline—from algorithm selection to report generation—making advanced causal methods accessible to researchers across all domains.
tags:
  - Causal Analysis
  - Machine Learning
  - Artificial Intelligence
  - Large Language Models
  - Autonomous Agent
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
  - icon: file-pdf
    icon_pack: fas
    name: Paper
    url: https://arxiv.org/abs/2504.13263
  - icon: youtube
    icon_pack: fab
    name: Video
    url: https://www.youtube.com/watch?v=A6j80I97Slg

url_code: ''
url_pdf: ''
url_slides: ''
url_video: ''

slides: ""
---

## The Challenge

Causal analysis is fundamental to scientific discovery and evidence-based decision-making. However, despite rapid advances in causal learning methods, a significant gap remains between theoretical sophistication and practical applicability. Domain experts often cannot leverage these powerful tools due to:

- **Algorithmic complexity**: 20+ methods with distinct assumptions and hyperparameters
- **Steep learning curves**: Requiring expertise in both causal theory and implementation
- **Configuration challenges**: Selecting appropriate methods for specific data characteristics

## Our Solution

**Causal-Copilot** is an LLM-powered autonomous agent that democratizes causal analysis by automating the entire analytical pipeline. Users simply upload their data and describe their analysis goals in natural language—Causal-Copilot handles the rest.

{{< figure src="projects/copilot/workflow-1.png" caption="End-to-end workflow: from natural language query to comprehensive causal analysis report" >}}

---

## System Architecture

Causal-Copilot is built on a modular architecture with five core components:

{{< figure src="projects/copilot/architecture-1.png" caption="Modular architecture of Causal-Copilot" >}}

| Module | Function |
|--------|----------|
| **User Interaction** | Natural language query parsing, domain knowledge integration, interactive feedback loop |
| **Preprocessing** | Data cleaning, schema extraction, statistical diagnostics (linearity, stationarity, heterogeneity) |
| **Algorithm Selection** | LLM-guided filtering, ranking based on data characteristics, hyperparameter configuration |
| **Postprocessing** | Bootstrap confidence evaluation, LLM-guided graph refinement, user revision loop |
| **Report Generation** | Causal graph visualization, result interpretation, LaTeX report compilation |

---

## Supported Algorithms

Causal-Copilot integrates **20+ state-of-the-art algorithms** across three categories:

### Causal Discovery

| Family | Algorithms | Data Type |
|--------|------------|-----------|
| Constraint-based | PC, FCI, CD-NOD, PCMCI | Tabular & Time Series |
| Score-based | GES, FGES, XGES, GRaSP | Tabular |
| Continuous Optimization | NOTEARS, GOLEM, CALM, CORL, DYNOTEARS | Tabular & Time Series |
| LiNGAM Family | ICA-LiNGAM, DirectLiNGAM, VAR-LiNGAM | Tabular & Time Series |
| MB-based | InterIAMB, IAMBnPC, HITON-MB, BAMB | Tabular |
| Granger Causality | Linear & Nonlinear Granger | Time Series |

### Causal Inference

| Method | Description |
|--------|-------------|
| **Double Machine Learning** | LinearDML, SparseLinearDML, CausalForestDML |
| **Doubly Robust Learning** | LinearDRL, SparseLinearDRL, ForestDRL |
| **Instrumental Variables** | DRIV Family (Linear, Sparse, Forest) |
| **Matching Methods** | PSM, CEM |
| **Counterfactual** | DoWhy-based counterfactual estimation |

### Auxiliary Analysis

- **Feature Importance**: SHAP-based attribution
- **Anomaly Attribution**: Causal structure-based root cause analysis

---

## Performance

Causal-Copilot consistently outperforms individual algorithms across diverse scenarios:

### Tabular Data (F1 Score)

| Scenario | Causal-Copilot | PC | FCI | GES | DirectLiNGAM |
|----------|----------------|-----|-----|-----|--------------|
| Default (p=10, n=1000) | 0.89 | 0.92 | 0.91 | 0.92 | 0.22 |
| Dense Graph (p=0.5) | **0.65** | 0.41 | 0.44 | 0.40 | 0.26 |
| Large Scale (p=50) | **0.94** | 0.70 | 0.79 | N/A | 0.23 |
| Super Large (p=100) | **0.90** | 0.68 | 0.74 | N/A | N/A |
| Extreme Large (p=500) | **0.60** | N/A | N/A | N/A | N/A |
| Non-Gaussian Noise | **0.97** | 0.84 | 0.85 | 0.86 | 0.57 |
| Heterogeneous Domains | **0.77** | 0.51 | 0.62 | 0.40 | 0.23 |
| Measurement Error | **0.86** | 0.69 | 0.80 | 0.79 | 0.28 |

### Time Series Data (F1 Score)

| Scenario | Causal-Copilot | PCMCI | DYNOTEARS | VARLiNGAM |
|----------|----------------|-------|-----------|-----------|
| Small (p=5, l=3) | **0.98** | 0.92 | 0.97 | 0.97 |
| Large Lag (l=20) | **0.85** | 0.84 | 0.77 | 0.77 |
| Very Large (p=100) | **0.18** | N/A | N/A | 0.12 |

---

## Interactive Demo

{{< figure src="projects/copilot/demo-1.png" caption="Web-based interface for interactive causal analysis" >}}

Try it yourself on [Hugging Face Space](https://huggingface.co/spaces/Causal-Copilot/Causal-Copilot).

---

## Sample Output

{{< figure src="projects/copilot/casestudy-1.png" caption="Example PDF report: dataset statistics, causal graph visualization, and analysis results" >}}

---

## Quick Start

```bash
# Command-line usage
python main.py --data_file data.csv --apikey YOUR_KEY --initial_query "Discover causal relationships"

# Web interface deployment
python Gradio/demo.py
```

---

## Citation

```bibtex
@article{causalcopilot2025,
  title={Causal-Copilot: An Autonomous Causal Analysis Agent},
  author={Wang, Xinyue and Zhou, Kun and Wu, Wenyi and others},
  journal={arXiv preprint arXiv:2504.13263},
  year={2025}
}
```
