---
layout: home
---

# Shaohui

This is a personal space for notes, modeling ideas and occasional thoughts.

Writing helps me think.

## Recent Posts

<ul>
  {% for post in site.posts %}
    <li>
      <a href="{{ post.url }}">{{ post.title }}</a> - {{ post.date | date: "%Y-%m-%d" }}
    </li>
  {% endfor %}
</ul>
