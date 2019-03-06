---
layout: default
date: 2019-02-26T00:10:14.395+00:00
title: 'Ceci n’est pas un website'
---
{% for collection in site.collections %}
  {% assign name = collection.label %}
  <h1>{{ name }}</h1>
  {% for item in site[name] %}
  <ul>
    <li><a href="{{ item.url | prepend: site.github.url }}">{{ item.date }} {{ item.title }}</a></li>
  </ul>
  {% endfor %}
{% endfor %}
