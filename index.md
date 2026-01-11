---
layout: page
title: Home
---

<!-- About Our Lab Section - Moved to Top -->
<section style="margin: 40px 0 60px;">
  <div style="background: white; padding: 40px 30px; border-radius: 12px; box-shadow: 0 4px 12px rgba(0, 0, 0, 0.08);">
    <h2 style="text-align: center; font-size: 2em; margin-bottom: 25px; color: #212121;">About Our Lab</h2>
    
    <!-- Team Photo -->
    <div style="text-align: center; margin-bottom: 30px;">
      <img src="/assets/images/team_gen_small.png" alt="Style Transfer Lab Team" style="max-width: 400px; width: 100%; height: auto; border-radius: 12px; box-shadow: 0 4px 12px rgba(0, 0, 0, 0.1);">
    </div>
    
    <p style="text-align: center; color: #757575; font-size: 1.05em; line-height: 1.7; max-width: 700px; margin: 0 auto 30px;">
      Style Transfer Lab is a collaborative research group specializing in generative AI, with a focus on color transfer, style transfer, and diffusion models. We bridge the gap between theoretical understanding and practical applications, developing innovative methods that appear in top-tier computer vision and machine learning venues.
    </p>
    <div style="text-align: center;">
      <a href="/about/" class="btn-primary">Meet Our Team →</a>
    </div>
  </div>
</section>

<!-- Hero Section -->
<div class="hero-section">
  <h1>Style Transfer Lab</h1>
  <p class="tagline">Advancing Generative AI Research Through Color Transfer, Style Transfer, and Diffusion Models</p>
  
  <div class="stats">
    <div class="stat-item">
      🎯 {{ site.papers | size }} Publications
    </div>
    <div class="stat-item">
      🏆 Top-Tier Venues: CVPR, ICML, AAAI
    </div>
    <div class="stat-item">
      🔬 Theory & Applications
    </div>
  </div>
  
  <div class="cta-buttons">
    <a href="/papers/" class="btn-primary">View Our Research</a>
    <a href="/about/#contact" class="btn-secondary">Collaborate With Us</a>
  </div>
</div>

<!-- Featured Papers Section -->
<section style="margin: 60px 0;">
  <h2 style="text-align: center; font-size: 2.5em; margin-bottom: 40px; color: #212121;">Featured Research</h2>
  
  <div class="papers-grid">
    {% assign featured_papers = site.papers | where: "featured", true | sort: 'year' | reverse %}
    {% for paper in featured_papers limit:3 %}
      <!-- Paper Card (inlined to avoid GitHub Pages include recursion limits) -->
      <div class="paper-card">
        {% if paper.image %}
          <img src="{{ paper.image }}" alt="{{ paper.title }}" class="paper-card-image">
        {% else %}
          <div class="paper-card-image" style="background: linear-gradient(135deg, #2196F3, #9C27B0);"></div>
        {% endif %}
        
        <div class="paper-card-content">
          <h3 class="paper-card-title">
            <a href="{{ paper.url }}">{{ paper.title }}</a>
          </h3>
          
          <div class="paper-card-authors">
            {{ paper.authors }}
          </div>
          
          <div class="paper-card-meta">
            {% if paper.conference %}
              {% assign conf_lower = paper.conference | downcase %}
              {% if conf_lower contains 'cvpr' %}
                <span class="venue-badge cvpr">CVPR {{ paper.year }}</span>
              {% elsif conf_lower contains 'icml' %}
                <span class="venue-badge icml">ICML {{ paper.year }}</span>
              {% elsif conf_lower contains 'aaai' %}
                <span class="venue-badge aaai">AAAI {{ paper.year }}</span>
              {% elsif conf_lower contains 'neurips' %}
                <span class="venue-badge neurips">NeurIPS {{ paper.year }}</span>
              {% elsif paper.venue_type == 'conference' %}
                <span class="venue-badge conference">{{ paper.conference }}</span>
              {% else %}
                <span class="venue-badge workshop">{{ paper.conference }}</span>
              {% endif %}
            {% endif %}
            
            {% if paper.year %}
              <span class="year-badge">{{ paper.year }}</span>
            {% endif %}
          </div>
          
          {% if paper.tags %}
            <div class="tags">
              {% for tag in paper.tags limit:3 %}
                <span class="tag">{{ tag }}</span>
              {% endfor %}
            </div>
          {% endif %}
          
          <p class="paper-card-abstract">
            {{ paper.abstract | strip_html | truncatewords: 30 }}
          </p>
        </div>
      </div>
    {% endfor %}
  </div>
  
  <div style="text-align: center; margin-top: 40px;">
    <a href="/papers/" class="btn-primary">See All Publications →</a>
  </div>
</section>

<!-- Research Themes Section -->
<section style="margin: 80px 0; background: linear-gradient(135deg, rgba(33, 150, 243, 0.05) 0%, rgba(156, 39, 176, 0.05) 100%); padding: 60px 20px; border-radius: 12px;">
  <h2 style="text-align: center; font-size: 2.5em; margin-bottom: 20px; color: #212121;">Research Themes</h2>
  <p style="text-align: center; color: #757575; font-size: 1.2em; margin-bottom: 40px; max-width: 700px; margin-left: auto; margin-right: auto;">
    Our work bridges theoretical foundations with practical applications in generative AI
  </p>
  
  <div class="themes-grid">
    <div class="theme-card">
      <div class="theme-card-icon">🎨</div>
      <h3 class="theme-card-title">Color & Style Transfer</h3>
      <p class="theme-card-description">
        Novel approaches for transferring color distributions and artistic styles using optimal transport, rectified flows, and diffusion guidance.
      </p>
      <a href="/research-themes/#color-transfer" class="theme-card-link">Explore Papers →</a>
    </div>
    
    <div class="theme-card">
      <div class="theme-card-icon">🤖</div>
      <h3 class="theme-card-title">Generative Models & Diffusion</h3>
      <p class="theme-card-description">
        Training-free guidance methods, diffusion-based inpainting, and understanding the geometry of generative model latent spaces.
      </p>
      <a href="/research-themes/#generative-models" class="theme-card-link">Explore Papers →</a>
    </div>
    
    <div class="theme-card">
      <div class="theme-card-icon">👔</div>
      <h3 class="theme-card-title">Computer Vision Applications</h3>
      <p class="theme-card-description">
        Real-world applications including virtual try-on for fashion, creative design tools, and biological data analysis.
      </p>
      <a href="/research-themes/#applications" class="theme-card-link">Explore Papers →</a>
    </div>
    
    <div class="theme-card">
      <div class="theme-card-icon">📐</div>
      <h3 class="theme-card-title">Theoretical Foundations</h3>
      <p class="theme-card-description">
        Mathematical analysis of latent space geometry, Fisher information metrics, and connections to statistical physics.
      </p>
      <a href="/research-themes/#theory" class="theme-card-link">Explore Papers →</a>
    </div>
  </div>
</section>


<!-- Latest Updates (if blog posts exist) -->
{% if site.posts.size > 0 %}
<section style="margin: 80px 0;">
  <h2 style="text-align: center; font-size: 2.5em; margin-bottom: 40px; color: #212121;">Latest Updates</h2>
  
  <div style="max-width: 800px; margin: 0 auto;">
    {% for post in site.posts limit:3 %}
      <div style="background: white; padding: 30px; border-radius: 12px; margin-bottom: 20px; box-shadow: 0 4px 12px rgba(0, 0, 0, 0.08); border-left: 4px solid #2196F3;">
        <h3 style="margin-top: 0;">
          <a href="{{ post.url }}" style="color: #212121; text-decoration: none;">{{ post.title }}</a>
        </h3>
        <p style="color: #757575; font-size: 0.9em; margin-bottom: 10px;">{{ post.date | date: "%B %d, %Y" }}</p>
        {% if post.excerpt %}
          <p style="color: #616161; line-height: 1.6;">{{ post.excerpt | strip_html | truncatewords: 30 }}</p>
        {% endif %}
      </div>
    {% endfor %}
  </div>
  
  <div style="text-align: center; margin-top: 30px;">
    <a href="/blog/" class="btn-secondary">View All Posts →</a>
  </div>
</section>
{% endif %}
