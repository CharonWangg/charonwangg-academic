---
title: 'Transformer Is Inherently a Causal Learner'
summary: We reveal that transformers trained autoregressively naturally encode causal structures—gradient attributions directly recover underlying causal graphs without any explicit causal objectives.
tags:
  - Causal Discovery
  - Transformers
  - Time Series
  - Foundation Models
  - Deep Learning
date: '2025-12-05T00:00:00Z'

# Optional external URL for project (replaces project detail page).
external_link: ''

image:
  size: actual
  caption: Transformers as Scalable Causal Learners
  focal_point: Smart

links:
  - icon: file-pdf
    icon_pack: fas
    name: Paper
    url: '#'  # TODO: Add paper URL when available
#  - icon: github
#    icon_pack: fab
#    name: Code
#    url: https://github.com/xxx/xxx

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

<!-- **Accepted to NeurIPS 2025 Workshop on CauScien: Uncovering Causality in Science** -->

What if the foundation models we use every day are secretly learning the causal structure of the world? We show that **transformers trained for prediction are inherently causal learners**—their gradient sensitivities reveal the true cause-and-effect relationships in data, without any explicit causal training objectives.

---

## The Big Picture

Causal discovery—figuring out what causes what—is fundamental to science. Traditional methods require specialized algorithms with strong assumptions. Meanwhile, transformers have become the backbone of modern AI, excelling at prediction tasks across domains.

**Our key insight**: These two worlds are deeply connected. When a transformer learns to predict the future from the past, it must implicitly learn which past variables actually matter for each prediction. This is exactly what causal discovery aims to find.

{{< figure src="projects/transformers-scale-discovery/overview.png" caption="**Data generation and transformer-based causal discovery.** Left: A decoder-only transformer trained for next-step prediction. Tokens are lagged observations; the model predicts X<sub>t</sub> from past values. Right: A lagged data-generating process. Each variable depends on selected past values per the true causal graph. The trained transformer learns the process, and relevance attribution helps recover the causal structure." >}}

---

## From Prediction to Causation

Consider a *p*-variate time series X<sub>t</sub> = (X<sub>1,t</sub>, ..., X<sub>p,t</sub>) and a lag window L ≥ 1. Each variable follows:

> X<sub>i,t</sub> = f<sub>i</sub>(Pa(i,t), U<sub>t</sub>, N<sub>i,t</sub>)

where Pa(i,t) are the lagged parents, U<sub>t</sub> are unobserved processes, and N<sub>i,t</sub> are mutually independent noises.

### Identifiability Assumptions

- **A1. Conditional Exogeneity**: Allows latent confounders as long as they don't create spurious dependencies
- **A2. No instantaneous effects**: All parents occur at lags ℓ ≥ 1
- **A3. Lag-window coverage**: The chosen L includes all true parents
- **A4. Faithfulness**: The distribution is faithful to the causal graph

### Theorem: Causal Identifiability via Prediction

> Under A1–A4 and regularity conditions, the lagged causal graph G* is **uniquely identifiable** via the score gradient energy: edge j → i at lag ℓ exists **if and only if** H<sup>ℓ</sup><sub>j,i</sub> := 𝔼[(∂<sub>x<sub>j,t-ℓ</sub></sub> log p(X<sub>i,t</sub> | X<sub>&lt;t</sub>))²] > 0.

This theorem characterizes causal parents through sensitivity of the conditional distribution to each input. Unlike classical Granger causality which tests mean prediction, the score gradient energy captures influence on the *entire* conditional distribution. **Gradient sensitivity = causal relevance.**

---

## Why Transformers Are Natural Causal Learners

We connect the identifiability theorem to decoder-only transformers through four key properties:

1. **Alignment with Identifiability**: Causal masking enforces temporal precedence (A2); the window L bounds maximum lag (A3); autoregressive training naturally fits conditional distributions

2. **Scalable Sparsity**: Finite capacity and weight decay compress observations into generalizable parameters; softmax attention induces competitive selection among candidates; multi-head context supports selecting complementary parents

3. **Contextual Parameters**: Attention matrices are input-conditioned, adapting to heterogeneity and non-stationarity—different contexts induce distinct dependency patterns, enabling a mixture-of-graphs view

4. **Gradient-Based Extraction**: We use Layer-wise Relevance Propagation (LRP) to compute how much each past variable contributes to each prediction, then aggregate and threshold to recover the causal graph

---

## Experimental Results

We evaluate decoder-only transformers against state-of-the-art causal discovery algorithms including PCMCI, DYNOTEARS, VAR-LiNGAM, NTS-NOTEARS, TCDF, and Granger causality tests.

### Overall Performance

{{< figure src="projects/transformers-scale-discovery/f1_analysis.png" caption="**F1 score analysis across regimes.** (A) Mean F1 across all experiments—DOT achieves 0.62, nearly doubling the best baseline. (B) High-dimensional: F1 vs. number of nodes. (C) Long-range dependencies: F1 vs. maximum lag. (D) Nonlinearity: F1 vs. functional forms. (E) Non-stationarity: F1 vs. number of domains. DOT stands for Decoder-only Transformer." >}}

The transformer recovers lagged parents accurately and consistently across settings, achieving **0.62 average F1**—nearly doubling the best baseline (DYNOTEARS at 0.37). Traditional methods degrade as dynamics and dimension grow, whereas the transformer remains robust without sensitive hyperparameter tuning.

---

### Modeling Nonlinear Interactions

We examine settings from simple to complex: linear, monotonic, piecewise linear, MLP with additive noise, and MLP with concatenated noise.

{{< figure src="projects/transformers-scale-discovery/nonlinear_scaling.png" caption="**Nonlinear dependencies.** F1 scores vs. sample size across different nonlinear settings. While traditional methods work efficiently in simple linear cases, transformers generally perform better as data scales, showing consistent accuracy improvement with more data." >}}

We observe a trade-off between data efficiency and expressivity. Traditional methods with simple estimators can achieve good performance efficiently in linear settings, but decoder-only transformers excel when modeling complex nonlinear dynamics and when data scales.

---

### Scaling in Non-Stationary Settings

We construct two types of non-stationarity: (1) regular setting with randomly sampled linear structures per domain, and (2) extreme setting with random structures and nonlinear functions per domain.

{{< figure src="projects/transformers-scale-discovery/nonstationary_scaling.png" caption="**Non-stationary dependencies.** F1 scores vs. sample size in different non-stationary settings. Unlike traditional methods that become intractable with more data, the transformer shows consistent improvement across sample sizes." >}}

Unlike traditional methods that become intractable with more data, **transformers exhibit scaling**—accuracy improves consistently with sample size. The model learns to handle multiple local mechanisms within a single framework, better separating and routing different causal structures as data increases.

---

### Robustness to Noise and Latent Variables

{{< figure src="projects/transformers-scale-discovery/latent_noise_robustness.png" caption="**Robustness to latent variables and noise.** Left: F1 scores with different amounts of latent variables. Right: F1 scores across different noise types (equal and non-equal variance). The transformer maintains stable performance across noise conditions but degrades with more latent confounders." >}}

Transformers demonstrate robust performance across different noise distributions, maintaining consistent accuracy regardless of noise type or variance properties. However, due to the lack of a latent variable modeling mechanism, transformers can learn spurious links when latent confounders are present.

---

### Handling Real-World Complications

{{< figure src="projects/transformers-scale-discovery/ablation_postprocessing.png" caption="**Handling violations of assumptions.** (a) Latent confounders: Post-processing with L-PCMCI substantially improves accuracy. (b) Instantaneous relationships: Combining with PCMCI+ refines the structure. (c) Domain indicators: Integrating known domain indices improves data efficiency in non-stationary settings." >}}

**Latent Confounders**: We show that post-processing with latent-aware methods like L-PCMCI, starting from transformer-predicted edges, sharply reduces the search space and yields substantially higher accuracy.

**Instantaneous Relationships**: By combining the learned structure with algorithms that handle contemporaneous relationships (e.g., PCMCI+), we can refine confounded graphs and recognize instantaneous effects.

**Domain Indicators**: Encoding domain indices as additional input helps the transformer separate cross-domain changes from invariants, improving data efficiency in non-stationary settings.

---

### Attention vs. Gradient Attribution

{{< figure src="projects/transformers-scale-discovery/transformer_variants.png" caption="**Transformer variants comparison.** Performance of different configurations (shallow vs. deep, LRP vs. attention scores) across long-range dependencies, nonlinearity, and non-stationarity. Deep transformers with LRP consistently outperform other variants." >}}

We find that raw attention scores work better in shallow (1-layer) transformers but fail in deeper models. As depth increases, repeated attention routing and residual MLP updates mix token representations, making attention unreliable for structure recovery. **LRP-based gradient attribution consistently outperforms attention-based methods**, especially in deep transformers suited for complex dynamics.

---

### Uncertainty Analysis

{{< figure src="projects/transformers-scale-discovery/uncertainty_mean.png" caption="**Uncertainty analysis (mean rankings).** Mean of relevance score rankings across samples. Higher values indicate stronger predicted causal relationships." >}}

{{< figure src="projects/transformers-scale-discovery/uncertainty_std.png" caption="**Uncertainty analysis (standard deviation).** Standard deviation of rankings across samples. Lower values indicate more consistent (confident) predictions." >}}

{{< figure src="projects/transformers-scale-discovery/uncertainty_combined.png" caption="**Combined uncertainty metric.** Mean over standard deviation of rankings with global top-k selection. True edges (green triangles) tend to have high mean rankings and low variance, indicating confident identification." >}}

Statistical causal discovery estimates uncertainty via resampling. With transformers, we aggregate per-sample estimates and use their standard deviation to gauge consistency. **True edges show higher mean rankings and lower variance**, offering a pragmatic way to surface reliable edges when precision is prioritized.

---

## Additional Analysis

### Intervention Effects Align with Gradient Attributions

To validate that gradient-based attributions truly capture causal relationships, we compare them with intervention-based effects (the gold standard in causal inference). We intervene on input variables by one standard deviation and measure the average effect on outputs.

{{< figure src="projects/transformers-scale-discovery/intervention_linear.png" caption="**Intervention effects vs. gradient attributions (linear case).** The intervention effect is strongly correlated with the relevance score, validating that gradient attributions recover true causal relationships." >}}

{{< figure src="projects/transformers-scale-discovery/intervention_nonlinear.png" caption="**Intervention effects vs. gradient attributions (nonlinear case).** The correlation remains strong even in nonlinear settings, implying consistency between the internal causal model and the learned structure." >}}

The strong correlation between intervention effects and gradient attributions confirms that **the transformer's internal representation genuinely captures causal structure**, not just statistical associations.

---

### Can Current Foundation Models Discover Structure Zero-Shot?

We explore whether existing time-series foundation models (Chronos2) can perform zero-shot causal discovery.

{{< figure src="projects/transformers-scale-discovery/foundation_model_zeroshot.png" caption="**Structure recovery with Chronos2 on linear data.** In zero-shot mode, Chronos2 uses a randomly initialized node-embedding layer. Under parameter-efficient finetuning, only normalization layers and the node-embedding layer are trained." >}}

**Key findings:**
- Zero-shot forecasting accuracy is reasonable but structure recovery is suboptimal
- Raw time-series data is less structured and noisier than language, making it hard to learn generalizable inductive biases
- Even with large-scale pretraining, effective sample size for learning dynamics is insufficient
- **Finetuning on domain-specific data significantly improves both forecasting and causal discovery**
- Adding node embeddings (even randomly initialized) helps the model distinguish variables and improves structure recovery

Current time-series foundation models can serve as noisy zero-shot discoverers but may require domain adaptation for practical applications.

---

### Realistic Non-Stationary Settings with Minimal Changes

Real-world systems often exhibit gradual, minimal changes across regimes rather than completely random structure shifts.

{{< figure src="projects/transformers-scale-discovery/lowdrift_minimal_changes.png" caption="**Performance under minimal regime changes.** Comparison of F1 scores between randomly sampled regime changes (original data) and minimal changes (low-drift data) where only a small part of the structure is rewired." >}}

When regime changes are minimal and gradual (more realistic), **data efficiency is substantially higher** compared to randomly sampled settings. This demonstrates the practical applicability of our approach to real-world scenarios where causal structures evolve slowly over time.

---

### Sensitivity Analysis: Graph Binarization

The choice of top-k in graph binarization affects the precision-recall trade-off.

{{< figure src="projects/transformers-scale-discovery/topk_sensitivity.png" caption="**Sensitivity of k choice in row-wise top-k binarization.** Smaller k emphasizes precision; larger k captures more potential parents. In linear cases where the model learns near-perfect structure, the choice of k significantly affects outcomes." >}}

{{< figure src="projects/transformers-scale-discovery/global_topk_sensitivity.png" caption="**Sensitivity of k choice in global top-k binarization.** Global top-k is more stable with respect to k choice and handles graphs with varied in-degrees better than row-wise top-k." >}}

**Recommendations:**
- Use **row-wise top-k** when variables have similar numbers of parents
- Use **global top-k** when parent counts vary across variables
- Visualize the heatmap of edge scores for flexible threshold selection based on task requirements (precision vs. recall)

---

<!-- ### CNN as Model Alternative

Our theoretical results apply to any architecture that can fit the data distribution. We test a simple 1D CNN as an alternative predictor.

{{< figure src="projects/transformers-scale-discovery/cnn_alternative.png" caption="**CNN as transformer alternative.** A 1D CNN performs comparably to deep transformers in many settings, especially when data is limited. Simpler models with stronger inductive bias can be more data-efficient." >}}

**Key insight:** When data is limited and noisy (low signal-to-noise ratio), simpler models with stronger inductive bias and lower parameter uncertainty achieve higher data efficiency for both forecasting and structure learning. We emphasize transformers for their **scaling potential** and ability to handle **multi-modal inputs** in the long run.

--- -->

## Implications

### For Causal Discovery
This work opens a **new paradigm**: instead of hand-crafting discovery algorithms, we can leverage the representation learning capabilities of foundation models. The transformer becomes a universal causal structure extractor that scales with data.

### For Foundation Models
The causal perspective offers new tools to **understand and improve** large models:
- **Interpretability**: Gradient attributions reveal learned dependencies
- **Hallucinations**: May arise when insufficient data prevents accurate structure learning—the model resorts to spurious correlations when it cannot adequately separate regimes
- **Architecture design**: Causal priors (sparsity, modularity) could guide better architectures

---

## Citation

```bibtex
@inproceedings{wang2025transformer,
  title={Transformer Is Inherently a Causal Learner},
  author={Wang, Xinyue and Wang, Stephen and Huang, Biwei},
  booktitle={NeurIPS 2025 Workshop on CauScien},
  year={2025}
}
```
