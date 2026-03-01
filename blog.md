---
layout: default
title: "Projects"
---

<article class="projects-shell">
  <header>
    <h1>Projects</h1>
    <p>A running archive of my research, coursework, and personal data projects.</p>
  </header>

  <div class="project-filters">
    <button class="filter-chip active" type="button" data-category="all">All</button>
    {% assign categories = site.posts | map: "categories" | join: "," | split: "," | uniq | sort %}
    {% for category in categories %}
      {% unless category == "" %}
      <button class="filter-chip" type="button" data-category="{{ category | strip | downcase }}">{{ category | strip }}</button>
      {% endunless %}
    {% endfor %}
  </div>

  <div class="project-grid">
    {% assign posts = site.posts | sort: "date" | reverse %}
    {% for post in posts %}
    {% assign category_slug = post.categories | join: "," | downcase %}
    <article class="project-card" data-categories="{{ category_slug }}">
      <p class="project-date">{{ post.date | date: "%B %d, %Y" }}</p>
      <h2><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h2>
      <p>{{ post.excerpt | strip_html | truncatewords: 26 }}</p>
      <div class="project-tags">
        {% for category in post.categories %}
        <span>{{ category }}</span>
        {% endfor %}
      </div>
    </article>
    {% endfor %}
  </div>
</article>

<script>
  document.addEventListener("DOMContentLoaded", function () {
    const buttons = document.querySelectorAll(".filter-chip");
    const cards = document.querySelectorAll(".project-card");

    buttons.forEach((button) => {
      button.addEventListener("click", () => {
        const selected = button.getAttribute("data-category");
        buttons.forEach((b) => b.classList.remove("active"));
        button.classList.add("active");

        cards.forEach((card) => {
          const categories = card
            .getAttribute("data-categories")
            .split(",")
            .map((value) => value.trim())
            .filter(Boolean);
          const visible = selected === "all" || categories.includes(selected);
          card.style.display = visible ? "block" : "none";
        });
      });
    });
  });
</script>
