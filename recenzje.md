---
layout: page
title: Recenzje
description: Recenzje polecanych przez nas książek
permalink: /recenzje/
---

{%- if site.posts.size > 0 -%}

  <ul class="post-list">
    {%- for post in site.posts -%}
    <li>
      {%- assign date_format = site.minima.date_format | default: "%b %-d, %Y"
      -%}
      <span class="post-meta">{{ post.date | date: date_format }}</span>
      <h3>
        <a class="post-link" href="{{ post.url | relative_url }}">
          {{ post.title | escape }}
        </a>
        <small>{{ post.description | escape }}</small>
      </h3>
      {%- if site.show_excerpts -%}
      {{ post.excerpt }}
      {%- endif -%}
    </li>
    {%- endfor -%}
  </ul>
  {%- endif -%}
