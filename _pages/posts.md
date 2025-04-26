---
permalink: /posts/
title: "Posts"
layout: default
---
<head>
  <link rel="stylesheet" href="{{ site.baseurl }}/assets/css/style.css">
</head>

<div class="posts-list">
  {% for post in site.posts %}
    <div class="post-preview">
      <h2><a href="{{ post.url }}" class="post-title">{{ post.title }}</a></h2>
      <p class="post-date">{{ post.date | date: "%B %d, %Y" }}</p>

      <!-- Preview (Excerpt) -->
      <div class="post-excerpt">
        {% if post.excerpt %}
          <p>{{ post.excerpt }}</p>
        {% else %}
          <!-- Leave it blank if no excerpt exists -->
        {% endif %}
      </div>

      <!-- Categories with links -->
      <div class="post-categories">
        {% if post.categories %}
          <ul class="categories-list">
            {% for category in post.categories %}
              <li class="category-item">
                <a href="/categories/{{ category | slugify }}" class="category-link">{{ category }}</a>
              </li>
            {% endfor %}
          </ul>
        {% endif %}
      </div>

      <a href="{{ post.url }}" class="read-more">Read more →</a>
    </div>
  {% endfor %}
</div>
