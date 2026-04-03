---
layout: home
title: ""
---

<div class="category-section">
  <h2>✈️ Travel</h2>
  <p class="category-desc">Real talk about traveling with a baby — what to pack, what to skip, and what nobody tells you.</p>
  {% assign travel_posts = site.posts | where_exp: "post", "post.categories contains 'travel'" | limit: 2 %}
  {% for post in travel_posts %}
  <article class="post-preview">
    <h3><a href="{{ post.url }}">{{ post.title }}</a></h3>
    <p>{{ post.excerpt | strip_html | truncate: 150 }}</p>
  </article>
  {% endfor %}
  <a href="/travel/" class="see-all">See all travel posts →</a>
</div>

<div class="category-section">
  <h2>👶 Life w Baby</h2>
  <p class="category-desc">What we bought, why and was it worth it.</p>
  {% assign prep_posts = site.posts | where_exp: "post", "post.categories contains 'life-w-baby'" | limit: 2 %}
  {% for post in prep_posts %}
  <article class="post-preview">
    <h3><a href="{{ post.url }}">{{ post.title }}</a></h3>
    <p>{{ post.excerpt | strip_html | truncate: 150 }}</p>
  </article>
  {% endfor %}
  <a href="/preparing-for-baby/" class="see-all">See all preparing for baby posts →</a>
</div>
