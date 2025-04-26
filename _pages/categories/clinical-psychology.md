---
title: "Clinical Psychology"
permalink: /categories/clinical-psychology/
layout: default
---
<head>
  <link rel="stylesheet" href="{{ site.baseurl }}/assets/css/style.css">
</head>

<h2>Posts in the Clinical Psychology Category</h2>

<div class="category-posts-list">
  {% assign category_posts = site.categories["Clinical Psychology"] %}
  {% for post in category_posts %}
    <div class="post-preview">
      <h2><a href="{{ post.url }}" class="post-title">{{ post.title }}</a></h2>
      <p class="post-date">{{ post.date | date: "%B %d, %Y" }}</p>
    </div>
  {% endfor %}
</div>
