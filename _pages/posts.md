---
permalink: /posts/
title: "Posts"
layout: default
---

{% for post in site.posts %}
  <div class="post-preview">
    <h2><a href="{{ post.url }}">{{ post.title }}</a></h2>
    <p class="post-date">{{ post.date | date: "%B %d, %Y" }}</p>

    <div class="post-excerpt">
      {% if post.excerpt %}
        <p>{{ post.excerpt }}</p>
      {% else %}
        <p>{{ post.content | strip_html | truncatewords: 40 }}</p>
      {% endif %}
    </div>

    <div class="post-categories">
      {% if post.categories %}
        <ul class="categories-list">
          {% for category in post.categories %}
            <li class="category-item">{{ category }}</li>
          {% endfor %}
        </ul>
      {% endif %}
    </div>

    <div class="post-media">
      {% if post.content contains "<img" %}
        <p>Embedded Image:</p>
        {{ post.content | remove: "<div class='image' >" | remove: "</div>" }}
      {% elsif post.content contains "<iframe" %}
        <p>Embedded Video/Content:</p>
        {{ post.content | strip_html }}
      {% endif %}
    </div>

    <a href="{{ post.url }}" class="read-more">Read more →</a>
  </div>
{% endfor %}
