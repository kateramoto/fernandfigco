---
layout: page
title: Preparing for Baby
permalink: /preparing-for-baby/
---

The research I did so you don't have to — registry lists, hospital bags, and everything in between.

{% assign prep_posts = site.posts | where_exp: "post", "post.categories contains 'preparing-for-baby'" %}
{% for post in prep_posts %}
  <article>
    <h3><a href="{{ post.url }}">{{ post.title }}</a></h3>
    <p>{{ post.excerpt | strip_html | truncate: 150 }}</p>
  </article>
{% endfor %}
