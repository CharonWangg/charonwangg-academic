---
# Custom Project Section with Timeline
widget: blank

# This file represents a page section.
headless: true

# Order that this section appears on the page.
weight: 65

title: Projects
subtitle: ''

design:
  columns: '1'
  spacing:
    padding: ['40px', '0', '40px', '0']
---

{{< rawhtml >}}
<div class="project-timeline-section">
  <!-- Filter Buttons -->
  <div class="project-filters">
    <button class="filter-btn active" data-filter="all">All</button>
    <button class="filter-btn" data-filter="causality">Causality</button>
    <button class="filter-btn" data-filter="world-model">World Model</button>
    <button class="filter-btn" data-filter="agent">Agent</button>
    <button class="filter-btn" data-filter="bci">Brain-Computer Interface</button>
  </div>

  <!-- Timeline -->
  <div class="project-timeline">
    <!-- 2025 -->
    <div class="timeline-year">
      <div class="year-marker">
        <span class="year-label">2025</span>
        <div class="year-line"></div>
      </div>

      <div class="project-grid">
        <!-- Transformer Causal Learner - 上下布局 -->
        <div class="project-card" data-category="causality">
          <div class="project-card-inner with-image layout-vertical">
            <div class="project-image">
              <a href="/project/transformers-scale-discovery/">
                <img src="/project/transformers-scale-discovery/featured.png" alt="Transformer Causal Learner">
              </a>
            </div>
            <div class="project-content">
              <div class="project-meta">
                <span class="project-date">Dec 2025</span>
                <span class="project-tag">Causality</span>
              </div>
              <h3 class="project-title">
                <a href="/project/transformers-scale-discovery/">Transformer Is Inherently a Causal Learner</a>
              </h3>
              <p class="project-summary">Transformers trained autoregressively naturally encode causal structures—gradient attributions directly recover underlying causal graphs.</p>
              <div class="project-links">
                <a href="#" class="project-link"><i class="fas fa-file-pdf"></i> Paper</a>
              </div>
            </div>
          </div>
        </div>

        <!-- WM3C - 左右布局 -->
        <div class="project-card" data-category="causality world-model">
          <div class="project-card-inner with-image layout-horizontal">
            <div class="project-image">
              <a href="/project/wm3c/">
                <img src="/project/wm3c/featured.png" alt="WM3C">
              </a>
            </div>
            <div class="project-content">
              <div class="project-meta">
                <span class="project-date">Feb 2025</span>
                <span class="project-tag">World Model</span>
                <span class="project-tag">Causality</span>
              </div>
              <h3 class="project-title">
                <a href="/project/wm3c/">WM3C: World Modeling with Compositional Causal Components</a>
              </h3>
              <p class="project-summary">A novel RL framework that enhances generalization to unseen environments through language-guided compositional causal components.</p>
              <div class="project-links">
                <a href="https://openreview.net/forum?id=XMgpnZ2ET7" target="_blank" class="project-link"><i class="fas fa-file-pdf"></i> Paper</a>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>

    <!-- 2024 -->
    <div class="timeline-year">
      <div class="year-marker">
        <span class="year-label">2024</span>
        <div class="year-line"></div>
      </div>

      <div class="project-grid">
        <!-- Causal-Copilot - 上下布局 -->
        <div class="project-card" data-category="causality agent">
          <div class="project-card-inner with-image layout-vertical">
            <div class="project-image">
              <a href="/project/copilot/">
                <img src="/project/copilot/featured.png" alt="Causal-Copilot">
              </a>
            </div>
            <div class="project-content">
              <div class="project-meta">
                <span class="project-date">Nov 2024</span>
                <span class="project-tag">Agent</span>
                <span class="project-tag">Causality</span>
              </div>
              <h3 class="project-title">
                <a href="/project/copilot/">Causal-Copilot: Autonomous Causal Analysis Agent</a>
              </h3>
              <p class="project-summary">A toolkit integrating LLM capabilities and domain expertise for automated causal analysis—enabling researchers to identify causal relationships through natural dialogue.</p>
              <div class="project-links">
                <a href="https://github.com/Lancelot39/Causal-Copilot" target="_blank" class="project-link"><i class="fab fa-github"></i> Code</a>
                <a href="https://huggingface.co/spaces/Causal-Copilot/Causal-Copilot" target="_blank" class="project-link"><i class="fas fa-rocket"></i> Demo</a>
                <a href="https://www.youtube.com/watch?v=A6j80I97Slg" target="_blank" class="project-link"><i class="fab fa-youtube"></i> Video</a>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>

    <!-- Earlier Projects -->
    <div class="timeline-year">
      <div class="year-marker">
        <span class="year-label">Earlier</span>
        <div class="year-line"></div>
      </div>

      <div class="project-grid">
        <!-- Learning Causal Discovery - 左右布局 -->
        <div class="project-card" data-category="causality">
          <div class="project-card-inner with-image layout-horizontal">
            <div class="project-image">
              <a href="/project/nmos6502/">
                <img src="/project/nmos6502/featured.png" alt="Learning Causal Discovery">
              </a>
            </div>
            <div class="project-content">
              <div class="project-meta">
                <span class="project-date">TMLR 2023</span>
                <span class="project-tag">Causality</span>
              </div>
              <h3 class="project-title">
                <a href="/project/nmos6502/">Learning Causal Discovery</a>
              </h3>
              <p class="project-summary">Learn to discover causality inside large complex systems without human prior—tested on MOS 6502 microprocessor.</p>
              <div class="project-links">
                <a href="https://github.com/KordingLab/LearningCausalDiscovery" target="_blank" class="project-link"><i class="fab fa-github"></i> Code</a>
                <a href="https://arxiv.org/abs/2209.05598" target="_blank" class="project-link"><i class="fas fa-file-pdf"></i> Paper</a>
              </div>
            </div>
          </div>
        </div>

        <!-- OpenBCI - 上下布局 -->
        <div class="project-card" data-category="bci">
          <div class="project-card-inner with-image layout-vertical">
            <div class="project-image">
              <a href="/project/openbci/">
                <img src="/project/openbci/featured.png" alt="OpenBCI Neural Feedback">
              </a>
            </div>
            <div class="project-content">
              <div class="project-meta">
                <span class="project-date">BIBE 2020</span>
                <span class="project-tag">Brain-Computer Interface</span>
              </div>
              <h3 class="project-title">
                <a href="/project/openbci/">Millisecond-level Phase Locked Neural Feedback</a>
              </h3>
              <p class="project-summary">A millisecond-level phase locked neural feedback system based on OpenBCI for real-time alpha wave regulation.</p>
              <div class="project-links">
                <a href="https://dl.acm.org/doi/pdf/10.1145/3431943.3432284" target="_blank" class="project-link"><i class="fas fa-file-pdf"></i> Paper</a>
              </div>
            </div>
          </div>
        </div>

        <!-- Sartorius - 左右布局 -->
        <div class="project-card" data-category="">
          <div class="project-card-inner with-image layout-horizontal">
            <div class="project-image">
              <a href="/project/sartorium/">
                <img src="/project/sartorium/featured.png" alt="Sartorius Segmentation">
              </a>
            </div>
            <div class="project-content">
              <div class="project-meta">
                <span class="project-date">Kaggle Top 1%</span>
                <span class="project-tag">Deep Learning</span>
              </div>
              <h3 class="project-title">
                <a href="/project/sartorium/">Sartorius Neuronal Cells Segmentation</a>
              </h3>
              <p class="project-summary">A robust deep learning pipeline for segmenting neuronal cells in microscopy images, achieving top 1% on Kaggle.</p>
              <div class="project-links">
                <a href="https://github.com/CharonWangg/Kaggle_Sartorius_Neurons_Segmentation" target="_blank" class="project-link"><i class="fab fa-github"></i> Code</a>
                <a href="https://drive.google.com/file/d/1QRQRx9shkoma-GDDAwCDP5JioBI8GZnu/view?usp=sharing" target="_blank" class="project-link"><i class="fas fa-file-pdf"></i> Paper</a>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</div>

<script>
document.addEventListener('DOMContentLoaded', function() {
  const filterBtns = document.querySelectorAll('.filter-btn');
  const projectCards = document.querySelectorAll('.project-card');
  const timelineYears = document.querySelectorAll('.timeline-year');

  filterBtns.forEach(btn => {
    btn.addEventListener('click', function() {
      // Update active button
      filterBtns.forEach(b => b.classList.remove('active'));
      this.classList.add('active');

      const filter = this.getAttribute('data-filter');

      // Filter cards
      projectCards.forEach(card => {
        const categories = card.getAttribute('data-category');
        if (filter === 'all' || categories.includes(filter)) {
          card.style.display = 'block';
          card.style.animation = 'fadeIn 0.3s ease';
        } else {
          card.style.display = 'none';
        }
      });

      // Hide empty year sections
      timelineYears.forEach(yearSection => {
        const visibleCards = yearSection.querySelectorAll('.project-card[style*="display: block"], .project-card:not([style*="display"])');
        let hasVisible = false;
        visibleCards.forEach(card => {
          if (card.style.display !== 'none') {
            hasVisible = true;
          }
        });
        yearSection.style.display = hasVisible ? 'block' : 'none';
      });
    });
  });
});
</script>
{{< /rawhtml >}}
