---
title: Foost Poetry Index
layout: base.njk
permalink: poems/index.html
---

<main>
  <div class="container">
    <div class="page-content">
      <h1>{{ title }}</h1>
      <p>Explore poems from the Foost community. This index lists all poems in the POETRY collection.</p>
      <div class="poem-grid">
        {% for poem in collections.poems %}
          <article class="poem-card">
            <h2><a href="{{ poem.url }}">{{ poem.data.title }}</a></h2>
            {% if poem.data.author %}
              <p class="poem-author">By {{ poem.data.author }}</p>
            {% endif %}
            {% if poem.data.tags %}
              <div class="poem-tags">
                {% for tag in poem.data.tags %}
                  <span class="tag">{{ tag }}</span>
                {% endfor %}
              </div>
            {% endif %}
          </article>
        {% endfor %}
      </div>
      <section class="poem-tags-section">
        <h2>Browse by Tags</h2>
        <div class="all-tags">
          {% set allTags = [] %}
          {% for poem in collections.poems %}
            {% for tag in poem.data.tags %}
              {% if tag not in allTags %}
                {% set allTags = allTags.concat([tag]) %}
              {% endif %}
            {% endfor %}
          {% endfor %}
          {% for tag in allTags | sort %}
            <a href="/poetry/tags/{{ tag | slugify }}/" class="tag-link">{{ tag }}</a>
          {% endfor %}
        </div>
      </section>
    </div>
  </div>
</main>
