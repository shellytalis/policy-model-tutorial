---
layout: dark
title: About
nav_order: 3
example: This is an example value.
---
About {{ site.title }}

{% comment %}

About {{ site.title }} by {{ site.author }}.
{{ page.example }}


{% include img-tiger.html %}

{% for animal in site.data.animals %}
- The {{ animal.name }} is a {{ animal.size }} animal.
{% endfor %}

{% for animal in site.data.animals %}
{% if animal.size == "large" %}- <strong style="color: {{ animal.color }};">{{ animal.name }}</strong>
{% else %}- <small>{{ animal.name }}</small>
{% endif %}
{% endfor %}

{% assign small_animals = site.data.animals | where: "size", "small" %}
{% for animal in small_animals %}
- {{ animal.name | upcase }}
{% endfor %}

{% endcomment %}
