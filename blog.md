---
layout: default
title: Blog
subtitle: Get the latest updates from the ΩZA Colony
permalink: /blog/
relativity: ..
action: "- Blog"
---
{%- if site.posts.size > 0 -%}
  {%- for post in site.posts -%}
    <div class="blog-card">
      {%- assign date_format = site.minima.date_format | default: "%b %-d, %Y" -%}
      <h3>{{ post.date | date: date_format }}</h3>
      <div class="blog-image" style="background-image: url({{ post.image }})"></div>
      <div class="blog-text">
        <a href="{{ post.url }}" class="blog-title">
          <h1>{{ post.title }}</h1>
        </a>
        <p>{{ post.body }}</p>
      </div>
    </div>
  {%- endfor -%}
{%- endif -%}
