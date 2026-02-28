---
layout: page
title: "About Me"
---

<section class="home-hero">
  <div class="home-hero-media">
    <img class="profile-photo" src="berkeley_headshot.JPG" alt="Headshot of Ajay Patel" width="240" height="240">
  </div>
  <div class="home-hero-copy">
    <p class="hero-kicker">Data Science · Machine Learning · Baseball Analytics</p>
    <p>
      Welcome to my personal website. I'm a current Junior Data Scientist with the Pittsburgh Pirates and a Master of Information and Data Science student at UC Berkeley. I earned my Bachelor's of Science in Data Science from the University of Rochester in December 2024.
    </p>
    <p>
      In the past, I've worked in data and analytics roles with the Los Angeles Dodgers, Optum, and ShotQuality. My work focuses on applied machine learning and data-driven decision-making, with a particular emphasis on baseball data.
    </p>
    <div class="hero-actions">
      <a class="hero-btn hero-btn-primary" href="/blog/">View Projects & Articles</a>
      <a class="hero-btn hero-btn-secondary" href="/resume/">View Resume</a>
    </div>
  </div>
</section>

<section class="home-highlights">
  <div class="highlight-card">
    <h3>Applied Modeling</h3>
    <p>Building practical predictive systems across sports, healthcare, and education-focused problems.</p>
  </div>
  <div class="highlight-card">
    <h3>Baseball Analytics</h3>
    <p>Research and tooling for pitch analysis, sequencing, player evaluation, and game-level decision support.</p>
  </div>
  <div class="highlight-card">
    <h3>End-to-End Projects</h3>
    <p>From data collection and feature engineering to model evaluation and production-ready interfaces.</p>
  </div>
</section>

<section class="home-recent">
  <div class="section-head">
    <h2>Recent Work</h2>
    <a href="/blog/">See all projects</a>
  </div>
  <div class="recent-grid">
    {% assign recent_posts = site.posts | sort: "date" | reverse %}
    {% for post in recent_posts limit: 3 %}
    <article class="recent-card">
      <p class="recent-date">{{ post.date | date: "%B %d, %Y" }}</p>
      <h3><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h3>
      <p>{{ post.excerpt | strip_html | truncatewords: 22 }}</p>
    </article>
    {% endfor %}
  </div>
</section>
