---
layout: home
title: "Shaohui"
description: "Personal notes and modeling thoughts."
---

# AI时代的“自留地”

This is a personal space for notes, modeling ideas and occasional thoughts.

Writing helps me think.

## Recent Posts

{% assign posts_sorted = site.posts | sort: 'date' | reverse %}
{% for post in posts_sorted %}
<div style="margin-bottom: 1.5em; padding-bottom: 0.5em; border-bottom: 1px solid #ddd;">
  <h3 style="margin:0;">
    <a href="{{ post.url }}">{{ post.title }}</a>
  </h3>
  <small>{{ post.date | date: "%Y-%m-%d" }}</small>
  {% if post.tags %}
    <p style="margin: 0.3em 0;">
      Tags: 
      {% for tag in post.tags %}
        <span style="background:#eee; padding:2px 6px; margin-right:3px; border-radius:3px;">{{ tag }}</span>
      {% endfor %}
    </p>
  {% endif %}
  {% if post.excerpt %}
    <p>{{ post.excerpt }}</p>
  {% else %}
    <p>{{ post.content | strip_html | truncate: 150 }}</p>
  {% endif %}
</div>
{% endfor %}
