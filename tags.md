---
layout: page
permalink: /tags/
title: Tags
---

<div class="category-posts">
  {% for tag in site.tags %}
    <h3 id="{{ tag[0] }}">{{ tag[0] }}</h3>
    <ul>
      {% for post in tag[1] %}
        <li><a href="{{ site.baseurl }}{{ post.url }}">{{ post.title }}</a><span class="cat-tag__date">{{post.date | date_to_string}}</span></li>
      {% endfor %}
    </ul>
  {% endfor %}
</div>