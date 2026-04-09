---
layout: page
title: Life w baby
permalink: /life-w-baby/
---

What we decided to buy, why and was it worth it.

{% assign prep_posts = site.posts | where_exp: "post", "post.categories contains 'life-w-baby'" %}
{% for post in prep_posts %}
  <article>
    <h3><a href="{{ post.url }}">{{ post.title }}</a></h3>
    <p>{{ post.excerpt | strip_html | truncate: 150 }}</p>
  </article>
{% endfor %}
