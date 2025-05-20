---
layout: page
title: Quantum Field Theory
permalink: /categories/qft/
---

# QFT
 
{% assign posts = site.categories.qft %}
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

