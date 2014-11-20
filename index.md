---
layout: page
title: Edgar Ortega
tagline: Blog de un desarrollador en PHP
description: Este es un sitio dedicado a el leguaje PHP y el Desarrollo de Software
---
{% include JB/setup %}

    
## Posts Recientes

<ul class="posts">
  {% for post in site.posts %}
    <li><span>{{ post.date | date_to_string }}</span> &raquo; <a href="{{ BASE_PATH }}{{ post.url }}">{{ post.title }}</a></li>
  {% endfor %}
</ul>
