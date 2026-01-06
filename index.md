---
title: Bio-inspired Robotics Lab
layout: default
---

<section class="hero">
  <div class="container hero-grid">
    <div class="hero-left">
      <img class="hero-logo" src="https://placehold.co/200x200?text=Lab+Logo" alt="Lab logo placeholder">
      <div>
        <h1 class="hero-title">Bio-Inspired Robotics Lab</h1>
        <p class="hero-subtitle">Biologically inspired robots for air, land, and sea — agile, adaptive, and efficient.</p>
        <p class="hero-subtitle">Replace this text and logo with your own lab details.</p>
      </div>
    </div>
    <div class="hero-media">
      <iframe src="https://www.youtube.com/embed/dQw4w9WgXcQ" title="Lab intro video" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
    </div>
  </div>
</section>

<section class="section">
  <div class="container section-grid">
    <div>
      <h2>Welcome</h2>
      <div class="card">
        <p>Welcome to the Bio-inspired Robotics Lab. We combine control theory, soft materials, and machine learning to create robots that adapt to complex environments. Swap this text with your lab overview to greet visitors.</p>
      </div>
    </div>
    <div>
      <h2>News &amp; Media</h2>
      <div class="card">
        {% for item in site.data.news limit:5 %}
        <div class="news-item">
          <p>{{ item.description }}</p>
          {% if item.link %}<a href="{{ item.link }}" target="_blank" rel="noopener">Watch video</a>{% endif %}
        </div>
        {% endfor %}
      </div>
    </div>
    <div>
      <h2>Research Highlights</h2>
      <div class="card">
        {% for project in site.data.publications limit:3 %}
        <div class="highlight-card">
          <img src="{{ project.thumbnail | default: 'https://placekitten.com/200/200' }}" alt="{{ project.title }} thumbnail">
          <div>
            <h3>{{ project.title }}</h3>
            <p>{{ project.summary }}</p>
            <div class="tag-list">
              {% for tag in project.tags %}
              <span class="tag">{{ tag }}</span>
              {% endfor %}
            </div>
          </div>
        </div>
        {% endfor %}
      </div>
    </div>
  </div>
</section>
