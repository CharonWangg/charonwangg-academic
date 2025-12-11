---
# Custom Contact Section - Minimalist Icon Grid
widget: blank

# This file represents a page section.
headless: true

# Order that this section appears on the page.
weight: 130

title: Get In Touch
subtitle: ''

design:
  columns: '1'
  spacing:
    padding: ['40px', '0', '60px', '0']
---

{{< rawhtml >}}
<div class="contact-section">
  <p class="contact-intro">
    I'm always happy to discuss research collaborations, academic opportunities, or just chat about causality and machine learning.
  </p>

  <div class="contact-grid">
    <a href="mailto:xiw159@ucsd.edu" class="contact-card" title="Email">
      <div class="contact-icon">
        <i class="fas fa-envelope"></i>
      </div>
      <span class="contact-label">Email</span>
      <span class="contact-value">xiw159@ucsd.edu</span>
    </a>

    <a href="https://twitter.com/CharonWangg" target="_blank" rel="noopener" class="contact-card" title="Twitter">
      <div class="contact-icon">
        <i class="fab fa-twitter"></i>
      </div>
      <span class="contact-label">Twitter</span>
      <span class="contact-value">@CharonWangg</span>
    </a>

    <a href="https://github.com/CharonWangg" target="_blank" rel="noopener" class="contact-card" title="GitHub">
      <div class="contact-icon">
        <i class="fab fa-github"></i>
      </div>
      <span class="contact-label">GitHub</span>
      <span class="contact-value">CharonWangg</span>
    </a>

    <a href="https://scholar.google.com/citations?hl=en&user=fLTrCAQAAAAJ" target="_blank" rel="noopener" class="contact-card" title="Google Scholar">
      <div class="contact-icon">
        <i class="fas fa-graduation-cap"></i>
      </div>
      <span class="contact-label">Scholar</span>
      <span class="contact-value">Publications</span>
    </a>

    <a href="https://www.linkedin.com/in/xinyue-wang-93011b1a9/" target="_blank" rel="noopener" class="contact-card" title="LinkedIn">
      <div class="contact-icon">
        <i class="fab fa-linkedin"></i>
      </div>
      <span class="contact-label">LinkedIn</span>
      <span class="contact-value">Connect</span>
    </a>

    <a href="https://www.kaggle.com/charonwangg" target="_blank" rel="noopener" class="contact-card" title="Kaggle">
      <div class="contact-icon">
        <i class="fab fa-kaggle"></i>
      </div>
      <span class="contact-label">Kaggle</span>
      <span class="contact-value">Competitions</span>
    </a>
  </div>

  <div class="contact-location">
    <i class="fas fa-map-marker-alt"></i>
    <span>University of California San Diego, La Jolla, CA</span>
  </div>
</div>
{{< /rawhtml >}}
