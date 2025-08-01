---
layout: default
title: Categories
permalink: /categories/
---

<div class="categories-list">
  {% for category in site.categories %}
  <div class="category-group">
    {% capture category_name %}{{ category | first }}{% endcapture %}
    <h2 id="{{ category_name | slugize }}">{{ category_name }}</h2>
    <a name="{{ category_name | slugize }}"></a>
    
    {% for post in site.categories[category_name] %}
    <article class="category-item">
      <h3><a href="{{ site.baseurl }}{{ post.url }}">{{ post.title }}</a></h3>
      <p class="post-meta">{{ post.date | date: "%B %-d, %Y" }}</p>
    </article>
    {% endfor %}
  </div>
  {% endfor %}
</div>
