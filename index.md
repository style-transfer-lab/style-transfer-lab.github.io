---
layout: home
title: Home
---

<div class="landing-page" id="top">
  <!-- HERO -->
  <section class="landing-hero" aria-label="Home hero">
    <div class="landing-container">
      <div class="landing-hero__grid">
        <div class="landing-hero__copy">
          <h1 class="landing-hero__title">Style Transfer Lab</h1>
          <p class="landing-hero__subtitle">
            We build mathematically rigorous generative AI methods grounded in <strong>optimal transport</strong>, <strong>information geometry</strong>, and <strong>latent space analysis</strong>—with applications in color/style transfer, biological data imputation, and lightweight on-device systems.
          </p>
          <div class="landing-hero__ctas">
            <a class="landing-btn landing-btn--primary" href="/papers/">Explore our research</a>
            <a class="landing-btn landing-btn--secondary" href="/about/#contact">Collaborate with us</a>
          </div>
        </div>

        <div class="landing-hero__visual">
          <img src="/assets/images/abstract_landing.png" alt="Style Transfer Lab research highlights">
        </div>
      </div>
    </div>
  </section>

  <!-- ABOUT -->
  <section class="landing-section" aria-label="About">
    <div class="landing-container">
      <div class="landing-section__header">
        <h2 class="landing-section__title">About our lab</h2>
      </div>
      <p class="landing-section__subtitle">
        Our work bridges theory and deployment: we develop principled models and algorithms, then validate them on real tasks and publish with clear artifacts (papers, code, and demos where possible).
      </p>

      <ul class="landing-pillars">
        <li class="landing-card landing-card__pad">
          <strong>Theory</strong><br>
          Optimal transport, geometry of probability, convergence guarantees.
        </li>
        <li class="landing-card landing-card__pad">
          <strong>Methods</strong><br>
          Diffusion/flows, guidance, latent space structure, training-free extensions.
        </li>
        <li class="landing-card landing-card__pad">
          <strong>Applications</strong><br>
          Color/style transfer, harmonization, biological data imputation, on-device inference.
        </li>
      </ul>
    </div>
  </section>

  <!-- PUBLICATIONS -->
  <section class="landing-section landing-section--muted" aria-label="Recent publications">
    <div class="landing-container">
      <div class="landing-section__header">
        <h2 class="landing-section__title">Recent publications</h2>
        <a class="landing-link" href="/papers/">View all</a>
      </div>

      {% assign home_papers = site.papers | where: "featured", true | sort: "year" | reverse %}
      {% if home_papers.size == 0 %}
        {% assign home_papers = site.papers | sort: "year" | reverse %}
      {% endif %}

      <div class="landing-publications" aria-label="Publication highlights">
        {% for paper in home_papers limit: 3 %}
          <article class="landing-card landing-publication-card">
            {% if paper.image %}
              <img class="landing-publication-card__media" src="{{ paper.image }}" alt="{{ paper.title }}">
            {% else %}
              <div class="landing-publication-card__media" style="background: linear-gradient(135deg, #2196F3, #9C27B0);"></div>
            {% endif %}

            <div class="landing-publication-card__body">
              <h3 class="landing-publication-card__title">
                <a href="{{ paper.url }}">{{ paper.title }}</a>
              </h3>

              <div class="landing-publication-card__meta">
                {% if paper.conference %}<span>{{ paper.conference }}</span>{% endif %}
                {% if paper.year %}<span>· {{ paper.year }}</span>{% endif %}
              </div>

              <p class="landing-publication-card__authors">{{ paper.authors }}</p>
              <p class="landing-publication-card__abstract">{{ paper.abstract | strip_html | truncatewords: 24 }}</p>

              <div class="landing-publication-card__links" aria-label="Paper links">
                {% if paper.arxiv %}<a href="{{ paper.arxiv }}" target="_blank" rel="noopener">arXiv</a>{% endif %}
                {% if paper.github %}<a href="{{ paper.github }}" target="_blank" rel="noopener">GitHub</a>{% endif %}
                {% if paper.openreview %}<a href="{{ paper.openreview }}" target="_blank" rel="noopener">OpenReview</a>{% endif %}
                {% if paper.pdf %}<a href="{{ paper.pdf }}" target="_blank" rel="noopener">PDF</a>{% endif %}
              </div>
            </div>
          </article>
        {% endfor %}
      </div>
    </div>
  </section>

  <!-- CONTACT -->
  <section class="landing-section" aria-label="Contact">
    <div class="landing-container">
      <div class="landing-section__header">
        <h2 class="landing-section__title">Get in touch</h2>
      </div>
      <p class="landing-section__subtitle">
        If you’re interested in collaboration, visiting positions, or consulting, send us a message—we’ll respond as soon as possible.
      </p>

      <div class="landing-contact" style="margin-top: 18px;">
        <div class="landing-card landing-card__pad">
          <form class="landing-form" action="mailto:your-email@example.com" method="post" enctype="text/plain">
            <div class="landing-form__row">
              <label for="name">Name *</label>
              <input type="text" id="name" name="name" required>
            </div>
            <div class="landing-form__row">
              <label for="email">Email *</label>
              <input type="email" id="email" name="email" required>
            </div>
            <div class="landing-form__row">
              <label for="message">Message *</label>
              <textarea id="message" name="message" rows="6" required></textarea>
            </div>
            <button class="landing-form__submit" type="submit">Send message</button>
          </form>
          <p style="margin: 12px 0 0; color: var(--text-secondary); font-size: 0.95em;">
            Email: <strong>your-email@example.com</strong>
          </p>
        </div>

        <div class="landing-card landing-card__pad">
          <p style="margin-top: 0;">
            Prefer browsing first?
          </p>
          <ul style="margin: 12px 0 0; padding-left: 18px; color: var(--text-secondary);">
            <li><a class="landing-link" href="/papers/">Research publications</a></li>
            <li><a class="landing-link" href="/about/">Team and mission</a></li>
            <li><a class="landing-link" href="/blog/">Lab notes</a></li>
          </ul>
          <p style="margin: 16px 0 0; color: var(--text-secondary); font-size: 0.95em;">
            (Replace placeholders with your official email + social links when ready.)
          </p>
        </div>
      </div>
    </div>
  </section>
</div>
