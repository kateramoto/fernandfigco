---
layout: page
title: Life with baby(x2)
permalink: /life-w-baby/
---

What we decided to buy, why and was it worth it.

{% assign prep_posts = site.posts | where_exp: "post", "post.categories contains 'preparing-for-baby'" %}
{% for post in prep_posts %}
  <article>
    <h3><a href="{{ post.url }}">{{ post.title }}</a></h3>
    <p>{{ post.excerpt | strip_html | truncate: 150 }}</p>
  </article>
{% endfor %}
