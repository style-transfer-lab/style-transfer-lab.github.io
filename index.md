---
layout: page
title: Home
---

# Welcome to Style Transfer Lab

We specialize in **computer vision research**, focusing on style transfer, generative models, and deep learning. 

## 🔬 Recent Papers
{% for paper in site.papers limit:3 %}
- **[{{ paper.title }}]({{ paper.url }})**  
  *{{ paper.authors }}* - {{ paper.conference }}
{% endfor %}

📖 **More publications**: [See all papers →](/papers/)

## ✍️ Latest Blog Posts
{% for post in site.posts limit:3 %}
- **[{{ post.title }}]({{ post.url }})** ({{ post.date | date: "%B %d, %Y" }})
{% endfor %}

[See all posts →](/blog/)
