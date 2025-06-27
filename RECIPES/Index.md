---
title: Foost Recipes
layout: base.njk
date: "Created"
permalink: recipes/index.html
---

<main>
  <div class="container">
    <div class="page-content">
      <h1>{{ title }}</h1>
      <p>Discover delicious recipes from the Foost community. Using the <a href="https://obsidian-recipe-view.readthedocs.io/en/latest/usage/features.html">Obsidian Reference View</a> format, these recipes work seamlessly with our foost.org website.</p>
      
      <div class="recipe-grid">
        {% for recipe in collections.recipes %}
          <article class="recipe-card">
            <h2><a href="{{ recipe.url }}">{{ recipe.data.title }}</a></h2>
            {% if recipe.data.aliases %}
              <p class="recipe-aliases">Also known as: {{ recipe.data.aliases | join(", ") }}</p>
            {% endif %}
            <div class="recipe-meta">
              {% if recipe.data['prep time'] %}<span class="prep-time">Prep: {{ recipe.data['prep time'] }}</span>{% endif %}
              {% if recipe.data['cook time'] %}<span class="cook-time">Cook: {{ recipe.data['cook time'] }}</span>{% endif %}
            </div>
            {% if recipe.data.tags %}
              <div class="recipe-tags">
                {% for tag in recipe.data.tags %}
                  <a href="/recipes/tags/{{ tag | slugify }}/" class="tag">{{ tag }}</a>
                {% endfor %}
              </div>
            {% endif %}
          </article>
        {% endfor %}
      </div>
      
      <section class="recipe-tags-section">
        <h2>Browse by Tags</h2>
        <div class="all-tags">
          {% set allTags = [] %}
          {% for recipe in collections.recipes %}
            {% for tag in recipe.data.tags %}
              {% if tag not in allTags %}
                {% set allTags = allTags.concat([tag]) %}
              {% endif %}
            {% endfor %}
          {% endfor %}
          {% for tag in allTags | sort %}
            <a href="/recipes/tags/{{ tag | slugify }}/" class="tag-link">{{ tag }}</a>
          {% endfor %}
        </div>
      </section>
    </div>
  </div>
</main>