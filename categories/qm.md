---
layout: page
title: Quantum Mechanics
permalink: /categories/qm/
---

# QFT
 
{% assign posts = site.categories.qm %}
{% assign books = posts | map: "book" | uniq %}

{% for book in books %}
## {{ book }}
<ul>
  {% for post in posts %}
    {% if post.book == book %}
    <li><a href="{{ post.url }}">{{ post.title }}</a></li>
    {% endif %}
  {% endfor %}
</ul>
{% endfor %}

