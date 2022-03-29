---
layout: default
title: Style
nav_order: 2
description: "Policy Models Tutorial."
---

## This is how you are going to write your css file!

To design the interview you want to embed, a css file is needed. The default file we provide - `style.css`, includes names of classes or IDs that express buttons, titles, paragraphs and so on. Each class or ID has its own design. You have the option to use or modify our default file. 
#### Pay attention! 
To change the file, the names of the classes or IDs must remain the same and only their design can be changed using css.

#### List of name of each class or ID and what it describes:

{% for btn in site.data.btn %}
- Description of the {{ btn.nameOfTheBtn }} calss that represents a button:
  {{ btn.description }}.
{% endfor %}

