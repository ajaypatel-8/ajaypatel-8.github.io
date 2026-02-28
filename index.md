---
layout: default
---

<section class="home-hero">
  <div class="home-hero-media">
    <img class="profile-photo" src="berkeley_headshot.JPG" alt="Headshot of Ajay Patel" width="240" height="240">
  </div>
  <div class="home-hero-copy">
    <p class="hero-kicker">Data Science · Machine Learning · Baseball Analytics</p>
    <p>
      Welcome to my personal website! I'm a current Junior Data Scientist with the Pittsburgh Pirates and a Master of Information and Data Science student at UC Berkeley. I earned my Bachelor's of Science in Data Science from the University of Rochester in December 2024.
    </p>
    <p>
      In the past, I've worked in data and analytics roles with the Los Angeles Dodgers, Optum, and ShotQuality. My work focuses on applied machine learning and data-driven decision-making, with a particular emphasis on baseball data.
    </p>
    <div class="hero-actions">
      <a class="hero-btn hero-btn-primary" href="/blog/">View Projects</a>
      <a class="hero-btn hero-btn-secondary" href="/resume/">View Resume</a>
    </div>
  </div>
</section>

<section class="home-highlights">
  <div class="highlight-card">
    <h3>Data Science</h3>
    <p>Applying statistics and machine learning to solve practical problems across sports, healthcare, and education.</p>
  </div>
  <div class="highlight-card">
    <h3>Baseball Analytics</h3>
    <p>Experience in two MLB front offices plus personal projects focused on player evaluation and game-level decision support.</p>
  </div>
  <div class="highlight-card">
    <h3>End-to-End Projects</h3>
    <p>From data collection and feature engineering to model evaluation and production-ready interfaces.</p>
  </div>
</section>

<section class="home-recent">
  {% assign featured_rain = site.posts | where_exp: "item", "item.path == '_posts/2026-02-28-207-final-project.md'" | first %}
  {% assign featured_bdb = site.posts | where_exp: "item", "item.path == '_posts/2024-01-06-bdb.md'" | first %}
  {% assign featured_scores = site.posts | where_exp: "item", "item.path == '_posts/2025-02-01-mlbScores.md'" | first %}
  <div class="section-head">
    <h2>Featured Work</h2>
    <a href="/blog/">See all projects</a>
  </div>
  <div class="recent-grid">
    <article class="recent-card">
      <h3><a href="{{ featured_rain.url | relative_url }}">Rainfall Prediction in Australia</a></h3>
      <p>Time-aware machine learning project using WeatherAUS data, sequence baselines, and latent-space methods to improve rain-day forecasting.</p>
    </article>
    <article class="recent-card">
      <h3><a href="{{ featured_bdb.url | relative_url }}">Scouting Opponents Through Expected YAC (NFL Big Data Bowl 2024)</a></h3>
      <p>Tracking-data modeling project for expected YAC and coaching-focused opponent scouting built for the NFL Big Data Bowl.</p>
    </article>
    <article class="recent-card">
      <h3><a href="{{ featured_scores.url | relative_url }}">MLB Scores Website</a></h3>
      <p>React application that surfaces daily MLB game results, previews, top performers, and game-level links for deeper analysis.</p>
    </article>
  </div>
</section>
