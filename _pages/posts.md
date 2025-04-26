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

      <div class="post-excerpt">
        {% if post.excerpt %}
          <p>{{ post.excerpt }}</p>
        {% else %}
          <p>{{ post.content | strip_html | truncatewords: 40 }}</p>
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

      <!-- Embedding Image or Video -->
      <div class="post-media">
        {% assign media_found = false %}
        {% for image in post.images %}
          {% if media_found == false %}
            <img src="{{ image }}" alt="Post Image" class="post-image">
            {% assign media_found = true %}
          {% endif %}
        {% endfor %}
        
        <!-- Handle Embedded Videos -->
        {% if post.content contains "<iframe" %}
          <div class="embedded-video">
            {% capture embedded_content %}
              {{ post.content | split: "</iframe>" | first }}
            {% endcapture %}
            {{ embedded_content }}
          </div>
        {% endif %}
      </div>

      <a href="{{ post.url }}" class="read-more">Read more →</a>
    </div>
  {% endfor %}
</div>
