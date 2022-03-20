---
layout: default
title: Style
nav_order: 2
description: "Policy Models Tutorial."
---

## This is how you are going to write your css file!

{% for btn in site.data.btn %}
- Description of the {{ btn.nameOfBtn }} button:
  {{ btn.description }}.
{% endfor %}

