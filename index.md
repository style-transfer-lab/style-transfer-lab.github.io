---
layout: home
title: Home
---

<style>
/* Scientific Letter Styling */
.scientific-page {
  font-family: Georgia, 'Times New Roman', serif;
  color: #2c3e50;
  line-height: 1.8;
  width: 100%;
  max-width: none;
}

.scientific-page h1, .scientific-page h2, .scientific-page h3 {
  font-family: Georgia, serif;
  font-weight: 600;
  color: #1a252f;
}

.lab-image-header {
  text-align: center;
  margin: 40px auto 30px;
  padding: 0 40px;
}

.lab-image-header img {
  max-width: 600px;
  width: 100%;
  height: auto;
  border-radius: 8px;
  box-shadow: 0 4px 12px rgba(0, 0, 0, 0.15);
}

.about-section {
  width: 100%;
  max-width: none;
  margin: 30px 0;
  padding-inline: clamp(16px, 4vw, 96px);
}

.about-section h1 {
  font-size: 2.2em;
  text-align: center;
  margin-bottom: 30px;
  border-bottom: 2px solid #34495e;
  padding-bottom: 15px;
}

.about-section p {
  font-size: 1.1em;
  color: #34495e;
  text-align: justify;
  width: 100%;
  max-width: none;
  margin: 0;
  line-height: 1.8;
}

.two-column-section {
  display: grid;
  grid-template-columns: 1.5fr 1fr;
  gap: 50px;
  width: 100%;
  max-width: none;
  margin: 60px 0;
  padding-inline: clamp(16px, 4vw, 96px);
}

@media (max-width: 768px) {
  .two-column-section { grid-template-columns: 1fr; }
}

.research-column h2, .contact-column h2 {
  font-size: 1.8em;
  margin-bottom: 25px;
  border-bottom: 1px solid #95a5a6;
  padding-bottom: 10px;
}

/* Compact Paper Cards */
.compact-paper-card {
  background: #ffffff;
  border: 1px solid #d0d0d0;
  border-radius: 4px;
  margin-bottom: 25px;
  overflow: hidden;
  transition: box-shadow 0.2s;
}

.compact-paper-card:hover {
  box-shadow: 0 2px 8px rgba(0, 0, 0, 0.12);
}

.compact-paper-image {
  width: 100%;
  height: 130px;
  object-fit: cover;
  background: #ecf0f1;
}

.compact-paper-content {
  padding: 18px;
}

.compact-paper-title {
  font-size: 1.15em;
  margin: 0 0 10px 0;
  font-weight: 600;
}

.compact-paper-title a {
  color: #2c3e50;
  text-decoration: none;
}

.compact-paper-title a:hover {
  color: #3498db;
  text-decoration: underline;
}

.compact-paper-meta {
  font-size: 0.9em;
  color: #7f8c8d;
  margin-bottom: 8px;
}

.compact-paper-authors {
  font-size: 0.95em;
  color: #555;
  margin-bottom: 10px;
  font-style: italic;
}

.compact-paper-abstract {
  font-size: 0.95em;
  color: #5a6c7d;
  line-height: 1.5;
  margin-top: 8px;
}

.venue-tag {
  display: inline-block;
  padding: 3px 10px;
  border-radius: 3px;
  font-size: 0.85em;
  font-weight: 500;
  background: #34495e;
  color: white;
  margin-right: 8px;
}

/* Contact Form Styling */
.contact-form {
  background: #f8f9fa;
  border: 1px solid #d0d0d0;
  border-radius: 4px;
  padding: 25px;
}

.form-group {
  margin-bottom: 18px;
}

.form-group label {
  display: block;
  margin-bottom: 6px;
  font-weight: 600;
  color: #2c3e50;
  font-size: 0.95em;
}

.form-group input,
.form-group textarea {
  width: 100%;
  padding: 10px;
  border: 1px solid #bdc3c7;
  border-radius: 3px;
  font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', sans-serif;
  font-size: 0.95em;
  box-sizing: border-box;
}

.form-group input:focus,
.form-group textarea:focus {
  outline: none;
  border-color: #3498db;
}

.submit-btn {
  width: 100%;
  padding: 12px;
  background: #34495e;
  color: white;
  border: none;
  border-radius: 3px;
  font-size: 1em;
  font-weight: 600;
  cursor: pointer;
  transition: background 0.2s;
}

.submit-btn:hover {
  background: #2c3e50;
}

.view-all-link {
  display: inline-block;
  margin-top: 20px;
  padding: 10px 20px;
  border: 1px solid #34495e;
  color: #34495e;
  text-decoration: none;
  border-radius: 3px;
  font-weight: 500;
  transition: all 0.2s;
}

.view-all-link:hover {
  background: #34495e;
  color: white;
}

.contact-info {
  margin-top: 20px;
  padding-top: 20px;
  border-top: 1px solid #d0d0d0;
  font-size: 0.9em;
  color: #555;
}
</style>

<div class="scientific-page">

<!-- Lab Team Image -->
<div class="lab-image-header">
  <img src="/assets/images/team_gen_small.png" alt="Style Transfer Lab Team">
</div>

<!-- About Our Lab - Full Width -->
<section class="about-section">
  <h1>Style Transfer Lab</h1>
  <p>
    Style Transfer Lab conducts research in optimal transport theory, information geometry, and latent space analysis of generative models. We develop mathematically rigorous frameworks with applications in color transfer, biological data imputation, and lightweight on-device implementations. Our work bridges theoretical foundations with practical deployments, publishing at top-tier venues including NeurIPS, ICML, and AAAI.
  </p>
</section>

<!-- Two-Column Layout: Research + Contact -->
<section class="two-column-section">
  
  <!-- Left Column: Featured Research -->
  <div class="research-column">
    <h2>Featured Research</h2>
    
    {% assign featured_papers = site.papers | where: "featured", true | sort: 'year' | reverse %}
    {% for paper in featured_papers limit:3 %}
      <div class="compact-paper-card">
        {% if paper.image %}
          <img src="{{ paper.image }}" alt="{{ paper.title }}" class="compact-paper-image">
        {% else %}
          <div class="compact-paper-image"></div>
        {% endif %}
        
        <div class="compact-paper-content">
          <h3 class="compact-paper-title">
            <a href="{{ paper.url }}">{{ paper.title }}</a>
          </h3>
          
          <div class="compact-paper-meta">
            {% if paper.conference %}
              <span class="venue-tag">{{ paper.conference }} {{ paper.year }}</span>
            {% endif %}
          </div>
          
          <div class="compact-paper-authors">
            {{ paper.authors }}
          </div>
          
          <p class="compact-paper-abstract">
            {{ paper.abstract | strip_html | truncatewords: 20 }}
          </p>
        </div>
      </div>
{% endfor %}

    <div style="text-align: center;">
      <a href="/papers/" class="view-all-link">View All Publications</a>
    </div>
  </div>
  
  <!-- Right Column: Get in Touch -->
  <div class="contact-column">
    <h2>Get in Touch</h2>
    
    <div class="contact-form">
      <form action="mailto:your-email@example.com" method="post" enctype="text/plain">
        
        <div class="form-group">
          <label for="name">Name *</label>
          <input type="text" id="name" name="name" required>
        </div>
        
        <div class="form-group">
          <label for="email">Email *</label>
          <input type="email" id="email" name="email" required>
        </div>
        
        <div class="form-group">
          <label for="message">Message *</label>
          <textarea id="message" name="message" rows="6" required></textarea>
        </div>
        
        <button type="submit" class="submit-btn">Send Message</button>
      </form>
      
      <div class="contact-info">
        <p><strong>Email:</strong> your-email@example.com</p>
        <p>We typically respond within 24-48 hours.</p>
      </div>
    </div>
    
    <div style="margin-top: 30px;">
      <p style="font-size: 0.95em; color: #555; line-height: 1.6;">
        Interested in research collaboration, consulting, or visiting positions? We welcome inquiries from academic and industry partners.
      </p>
      <a href="/about/" class="view-all-link" style="margin-top: 15px;">Learn More About Our Team</a>
    </div>
  </div>
  
</section>

</div>
