---
layout: default
title: Tags
permalink: /tags/
---

<div class="tags-page">
  <div class="tags-list">
    {% assign sorted_tags = site.tags | sort %}
    {% for tag in sorted_tags %}
      {% assign tag_name = tag[0] %}
      <div class="tag-group">
        <h2 id="{{ tag_name | slugize }}">
          <a class="tag-anchor" href="#{{ tag_name | slugize }}">#</a>
          {{ tag_name }}
        </h2>
        
        <ul class="tag-posts">
          {% for post in site.tags[tag_name] %}
            <li>
              <a href="{{ post.url }}">{{ post.title }}</a>
              <small>{{ post.date | date: "%b %-d, %Y" }}</small>
            </li>
          {% endfor %}
        </ul>
      </div>
    {% endfor %}
  </div>
</div>
