---
layout: post
title: Classical Mechanics
permalink: /categories/mechanics/
---

# Classical Mechanics

{% assign posts = site.categories.mechanics %}
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

