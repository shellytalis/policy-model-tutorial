---
layout: default
title: About
nav_order: 5
example: This is an example value.
---

{% comment %}

About {{ site.title }}

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

**PolicyModels** is a system that uses a formal model to identify situations of specific cases as legal systems by interviewing each person’s case.

