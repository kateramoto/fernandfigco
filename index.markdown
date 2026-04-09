---
layout: home
title: ""
---

<!-- FEATURED POST -->
{%- assign featured = site.posts | first -%}
{%- if featured -%}
<div class="category-section" style="padding-top: 4rem; border-top: none;">
  <a href="{{ featured.url | relative_url }}" class="post-featured">
    <div class="post-featured__image-wrap">
      {%- if featured.image -%}
        <img src="{{ featured.image | relative_url }}" alt="{{ featured.title }}" loading="eager">
      {%- endif -%}
    </div>
    <div class="post-featured__body">
      <p class="post-featured__meta">
        {{ featured.categories | first | capitalize }} &nbsp;&middot;&nbsp;
        {{ featured.date | date: "%B %-d, %Y" }}
      </p>
      <h2 class="post-featured__title">{{ featured.title }}</h2>
      <p class="post-featured__excerpt">{{ featured.excerpt | strip_html | truncatewords: 35 }}</p>
      <span class="post-card__read-more">Read more</span>
    </div>
  </a>
</div>
{%- endif -%}

<!-- TRAVEL SECTION -->
{%- assign travel_posts = site.posts | where_exp: "post", "post.categories contains 'travel'" | limit: 3 -%}
{%- if travel_posts.size > 0 -%}
<div class="category-section">
  <div class="section-label"><h2>Travel</h2></div>
  <div class="posts-grid">
    {%- for post in travel_posts -%}
    <a href="{{ post.url | relative_url }}" class="post-card">
      <div class="post-card__image-wrap {% unless post.image %}post-card__image-wrap--empty{% endunless %}">
        {%- if post.image -%}
          <img src="{{ post.image | relative_url }}" alt="{{ post.title }}" loading="lazy">
        {%- endif -%}
      </div>
      <p class="post-card__meta">{{ post.date | date: "%B %-d, %Y" }}</p>
      <h3 class="post-card__title">{{ post.title }}</h3>
      <p class="post-card__excerpt">{{ post.excerpt | strip_html | truncatewords: 22 }}</p>
      <span class="post-card__read-more">Read more</span>
    </a>
    {%- endfor -%}
  </div>
  <div class="see-all"><a href="{{ '/travel/' | relative_url }}">See all travel posts</a></div>
</div>
{%- endif -%}

<!-- LIFE W BABY SECTION -->
{%- assign baby_posts = site.posts | where_exp: "post", "post.categories contains 'life-w-baby'" | limit: 3 -%}
{%- if baby_posts.size > 0 -%}
<div class="category-section">
  <div class="section-label"><h2>Life w Baby</h2></div>
  <div class="posts-grid">
    {%- for post in baby_posts -%}
    <a href="{{ post.url | relative_url }}" class="post-card">
      <div class="post-card__image-wrap {% unless post.image %}post-card__image-wrap--empty{% endunless %}">
        {%- if post.image -%}
          <img src="{{ post.image | relative_url }}" alt="{{ post.title }}" loading="lazy">
        {%- endif -%}
      </div>
      <p class="post-card__meta">{{ post.date | date: "%B %-d, %Y" }}</p>
      <h3 class="post-card__title">{{ post.title }}</h3>
      <p class="post-card__excerpt">{{ post.excerpt | strip_html | truncatewords: 22 }}</p>
      <span class="post-card__read-more">Read more</span>
    </a>
    {%- endfor -%}
  </div>
  <div class="see-all"><a href="{{ '/life-w-baby/' | relative_url }}">See all posts</a></div>
</div>
{%- endif -%}
