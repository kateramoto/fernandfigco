---
layout: page
title: Travel
permalink: /travel/
---

Everything I learned about traveling with a baby — from the first flight to family road trips.

{% assign travel_posts = site.posts | where_exp: "post", "post.categories contains 'travel'" %}
{% for post in travel_posts %}
  <article>
    <h3><a href="{{ post.url }}">{{ post.title }}</a></h3>
    <p>{{ post.excerpt | strip_html | truncate: 150 }}</p>
  </article>
{% endfor %}
