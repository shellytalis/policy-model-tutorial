---
layout: default
title: Style
nav_order: 2
description: "Policy Models Tutorial."
---

## This is how you are going to write your css file!

To design the interview you want to embed, a css file is needed. 

In the html file, in the *head* tag, you need to add the following line for the design. 

```yaml
  <link rel="stylesheet" href= ${nameOfTheCssFile} >
```
This link tag is a link to an external style sheet. 

* In case of the ***["Default" web component](style.html#default-web-component)***, the default file we provide is `styleDefault.css`.

* In case of the ***["Chat" web component](style.html#chat-web-component)***, the default file we provide is `styleChat.css`.

Each file includes names of classes or IDs that express buttons, titles, paragraphs and so on. Each class or ID has its own design. You have the option to use or modify our default file. 

**Pay attention!** 

To change the file, the names of the classes or IDs must remain the same and **only** their design can be changed using css.

----

## *"Default" web component*

----


**List of name of each button and what it describes:**

{% for btn in site.data.btnDefault %}
- Description of the **{{ btn.nameOfTheBtn }}** class that represents a button:
  {{ btn.description }}.
{% endfor %}

**List of name of each class and what it describes:**

{% for class in site.data.classDefault %}
- Description of the **{{ class.nameOfTheClass }}** class:
  {{ class.description }}.
{% endfor %}

**List of name of each id and what it describes:**

{% for id in site.data.idDefault %}
- Description of the **{{ id.nameOfTheID }}** id:
  {{ id.description }}.
{% endfor %}


----

## *"Chat" web component*

----


**List of name of each button and what it describes:**

{% for btn in site.data.btnChat %}
- Description of the **{{ btn.nameOfTheBtn }}** class that represents a button:
  {{ btn.description }}.
{% endfor %}

**List of name of each class and what it describes:**

{% for class in site.data.classChat %}
- Description of the **{{ class.nameOfTheClass }}** class:
  {{ class.description }}.
{% endfor %}

**List of name of each id and what it describes:**

{% for id in site.data.idChat %}
- Description of the **{{ id.nameOfTheID }}** id:
  {{ id.description }}.
{% endfor %}

----

### Note

In both web components, _Default_ and _Chat_ web components, in our html files there are **link** tags. 

The `<link rel="stylesheet" href="styleDefault.css">` (in case of _Default_ web component) or `<link rel="stylesheet" href="styleChat.css">` (in case of _Chat_ web component) link tag is a link to an external style sheet. 

The other link tags are necessary for the font of the text of the interview.

All this files you can find in our [GitHub](https://github.com/EilonBenIshay/PolicyModelsProjectFrontend2022).

----

### Pay Attention

All content, like the content inside a button or titles, is saved in attributes in a class called `TextAssets.js`.
An explanation of each variable can be found [here](https://shellytalis.github.io/policy-model-tutorial/textAssets.html).

----
