# Hero Section Refresh — Research Landscape & Wording (as of 2025-12-15)

Goal: update the homepage “hero/About” so it’s **less niche than “strong causality”**, while still being **honest** about what you’ve actually built recently: *scalable causal learning + world models + agents*.

This note has two parts:
1) What your **recent projects (≈ last 3 years)** already signal.
2) What “frontier labs” (DeepMind / Microsoft Research / Meta FAIR / OpenAI) publicly emphasize, and the **keywords/phrases** they use — as raw material for the most *clear, contemporary wording*.

---

## 1) Your recent work signals (Selected Projects, 2023–2025)

### 2025 — Transformer Is Inherently a Causal Learner
- **Theme**: *foundation models for structure learning* — using autoregressive transformers + attribution to recover causal graphs.
- **Signals**:
  - “Scalable” / “data-driven” causal discovery (learning, not hand-designed procedures)
  - “Foundation models for time series” / “representation learning as discovery”
  - Bridges **interpretability** ↔ **structure / mechanisms**
- Project page: `/content/project/transformers-scale-discovery/index.md`

### 2025 — WM3C: Language-guided Composable Causal Components (World Modeling + RL)
- **Theme**: *world models for generalization* — compositional causal components + language as a compositional scaffold.
- **Signals**:
  - World modeling as a route to **OOD / unseen environment generalization**
  - “Composable / modular” latent structure with identifiability flavor
  - Positioned naturally at the **world model ↔ agent** interface
- Project page: `/content/project/wm3c/index.md`

### 2024 — Causal-Copilot: Autonomous Causal Analysis Agent
- **Theme**: *agentic scientific workflow automation* — an LLM agent that plans and executes a causal analysis pipeline end-to-end.
- **Signals**:
  - “Agent” framing is not marketing: it’s literally orchestration, tool use, and report generation
  - Emphasizes **systems + UX** for research, not only theory
  - A strong bridge from “causality” to “agents” without losing identity
- Project page: `/content/project/copilot/index.md`

### 2023 — Learning domain-specific causal discovery from time series
- **Theme**: *learned causal discovery* (domain-specific procedures learned from data) rather than human-crafted algorithms.
- **Signals**:
  - “Causal discovery at scale” via learning + domain adaptation
  - Strong empirical orientation; fits the “scalable causal learning” narrative
- Project page: `/content/project/nmos6502/index.md`

**Bottom line**: you already have credible “hooks” for all three target interests:
- **Scalable causal learning** (learned discovery; transformers as scalable structure learners)
- **World models** (WM3C; generalization to unseen environments)
- **Agents** (Causal-Copilot; pipeline automation; tool use)

---

## 2) Frontier labs: recurring themes + wording (with links)

This section is deliberately keyword-focused: collect “how they say it” rather than over-explaining.

### Google DeepMind
Observed emphasis (public-facing):
- **World models / simulators**: “world models”, “simulate”, “physical world”
- **Agents + interaction**: “AI agent”, “human-agent interaction”, “universal AI assistant”
- **Physical AI / robotics**: robotics-centric multimodal models and demos
- **Agentic coding**: explicit “coding agent” framing (algorithms/design)

Sources (current URLs):
- DeepMind blog index: https://deepmind.google/discover/blog/
- “Genie 3: A new frontier for world models”: https://deepmind.google/blog/genie-3-a-new-frontier-for-world-models/
- “SIMA 2: A Gemini-Powered AI Agent for 3D Virtual Worlds”: https://deepmind.google/blog/sima-2-an-agent-that-plays-reasons-and-learns-with-you-in-virtual-3d-worlds/
- “AlphaEvolve: A Gemini-powered coding agent…”: https://deepmind.google/blog/alphaevolve-a-gemini-powered-coding-agent-for-designing-advanced-algorithms/
- Project Astra (universal assistant framing): https://deepmind.google/models/project-astra/
- Project Mariner (human-agent interaction / browser use): https://deepmind.google/models/project-mariner/
- Gemini Robotics: https://deepmind.google/models/gemini-robotics/
- DeepMind research “Projects”: https://deepmind.google/research/projects/

### Microsoft Research / AI Frontiers
Observed emphasis (public-facing):
- **Agentic systems**: “agentic”, “multi-agent system”, “agentic workflows”
- **Computer use**: “computer use” as a concrete agent capability (UI / browser / tools)
- **Evaluation & environments**: simulation environments for studying agents

Sources (current URLs):
- AI Frontiers lab page: https://www.microsoft.com/en-us/research/lab/ai-frontiers/
- Microsoft Research project “Agent AI”: https://www.microsoft.com/en-us/research/project/agent-ai/
- “Magentic-One: A generalist multi-agent system…”: https://www.microsoft.com/en-us/research/articles/magentic-one-a-generalist-multi-agent-system-for-solving-complex-tasks/
- “FARA-7B: An efficient agentic model for computer use”: https://www.microsoft.com/en-us/research/blog/fara-7b-an-efficient-agentic-model-for-computer-use/
- “Magentic Marketplace: … simulation environment … agentic markets”: https://www.microsoft.com/en-us/research/blog/magentic-marketplace-an-open-source-simulation-environment-for-studying-agentic-markets/

### Meta AI / FAIR
Observed emphasis (public-facing):
- **World models**: explicit “world model” framing (e.g., V-JEPA 2; physical reasoning; robot planning)
- **Agentic stack / infra**: “agentic AI” as systems + runtime + orchestration
- **Open research**: “innovating in the open”, AMI framing

Sources:
- Meta AI blog “Introducing the V-JEPA 2 world model…”: https://ai.meta.com/blog/v-jepa-2-world-model-benchmarks/
- Meta AI blog “The Building Blocks of Agentic AI: From Kernels to Clusters”: https://ai.meta.com/blog/introducing-pytorch-native-agentic-stack/
- Meta AI blog “Agents Rule of Two: A Practical Approach to AI Agent Security”: https://ai.meta.com/blog/practical-ai-agent-security/
- Meta AI “AI Research” overview: https://ai.meta.com/research/

### OpenAI
Observed emphasis (public-facing):
- **Reasoning models**: explicit “o series” alongside frontier GPT models
- **World simulators**: “world simulators” framing for video generation models (Sora)
- **Agents**: explicit agent platform framing (workflows, tools, reliability)
- **Safety / evaluations**: system cards as part of public communication

Sources:
- OpenAI “Research” landing: https://openai.com/research/
- “Video generation models as world simulators” (Sora technical report): https://openai.com/index/video-generation-models-as-world-simulators/
- “Sora: Creating video from text” (public page): https://openai.com/index/sora/
- “OpenAI o3 and o4-mini” (reasoning model series): https://openai.com/index/introducing-o3-and-o4-mini/
- OpenAI “Agent Platform”: https://openai.com/agent-platform/
- “Deep research system card” (Feb 25, 2025): https://openai.com/index/deep-research-system-card/

### Anthropic (optional extra signal for “frontier wording”)
Observed emphasis (public-facing):
- **Alignment** and **interpretability** as first-class research directions
- Research framing tends to use: “alignment”, “interpretability”, “model behavior”, “societal impacts”

Sources:
- Anthropic “Research” landing: https://www.anthropic.com/research
- Anthropic “Interpretability” team: https://www.anthropic.com/research/team/interpretability
- “Project Fetch: Can Claude train a robot dog?”: https://www.anthropic.com/research/project-fetch-robot-dog
- “Tracing the thoughts of a large language model”: https://www.anthropic.com/research/tracing-thoughts-language-model

---

## 3) Cross-lab keyword map (good hero-section raw material)

### Foundation model framing (broad, non-niche)
- *foundation models*, *scaling*, *representation learning*, *multimodal*, *reasoning*

### World model framing (forward-looking, aligns with embodied + planning)
- *world model*, *world simulator*, *physical world*, *physical reasoning*, *simulate*, *predict*, *plan*, *generalization*, *OOD / unseen environments*

### Agent framing (industry-recognizable, matches “agents” wave)
- *agentic*, *generalist agent*, *multi-agent*, *computer use*, *tool use*, *workflows*, *orchestration*, *human-agent interaction*, *reliability / robustness*

### Reliability / safety framing (optional, but increasingly common)
- *reliability*, *robustness*, *alignment*, *safety*, *interpretability*, *system card*, *evaluations*

### Causality framing (keep it, but make it enabling rather than the whole identity)
- *causality-aware*, *structure learning*, *mechanisms*, *interventions*, *robust generalization*

Practical implication for your positioning:
- “Causality” reads niche if it’s the **noun** in every sentence.
- “Causality-aware” / “structure learning” reads broader if it’s the **adjective** enabling world models + agents.

---

## 4) Hero copy templates (candidate wordings)

Pick one “vibe” and keep it short. The about widget can do: (headline-ish sentence) + (1–2 short lines) + (3–5 interests).

### Template A — crisp, frontier-aligned
> I build scalable causal learning methods for world models and agentic decision-making.

Support line options:
- “I’m interested in how foundation models can learn *structured, transferable* representations of dynamics and mechanisms.”
- “My work spans causal discovery with foundation models, causality-guided world modeling in RL, and agents for scientific workflows.”

### Template B — world-model-forward (causality as a tool, not the label)
> I study how to learn world models that support reliable agents.

Support line options:
- “I use causal structure learning to make world models more interpretable, generalizable, and controllable.”

### Template C — agent-forward (good if recruiting/industry)
> I build agents that reason over structure: data → mechanisms → decisions.

Support line options:
- “From causal discovery to causality-aware world models, to agentic systems for end-to-end analysis.”

### Template D — structure-first (broad, but still technical)
> I work on scalable structure learning for foundation models, world models, and agents.

Support line options:
- “I use causal learning as a tool for robust generalization and reliable decision making.”

---

## 5) “Interests” list suggestions (About widget)

Keep these modern + broad, and let projects prove the “causality” depth.

Option 1 (balanced):
- Scalable Causal Learning
- World Models
- Agentic Systems
- Foundation Models

Option 2 (world-model heavy):
- World Models & Model-based RL
- Structure / Mechanism Learning
- Agents & Planning
- Multimodal Learning

Option 3 (agent + science heavy):
- Agentic Scientific Workflows
- Causal Discovery & Inference
- Robust Generalization
- Foundation Models
