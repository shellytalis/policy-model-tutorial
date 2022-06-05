---
layout: default
title: Style
nav_order: 2
description: "Policy Models Tutorial."
---

## This is how you are going to write your css file!

To design the interview you want to embed, a css file is needed. 

In case of the **"Default" web component**, the default file we provide is `styleDefault.css`.

In case of the **"Chat" web component**, the default file we provide is `styleChat.css`.

Each file includes names of classes or IDs that express buttons, titles, paragraphs and so on. Each class or ID has its own design. You have the option to use or modify our default file. 
**Pay attention!** To change the file, the names of the classes or IDs must remain the same and only their design can be changed using css.

## "Default" web component

**List of name of each button and what it describes:**

{% for btn in site.data.btnDefault %}
- Description of the **{{ btn.nameOfTheBtn }}** class that represents a button:
  {{ btn.description }}.
{% endfor %}

**List of name of each class in div and what it describes:**

{% for class in site.data.classDefault %}
- Description of the **{{ class.nameOfTheClass }}** class:
  {{ class.description }}.
{% endfor %}

**List of name of each id and what it describes:**

{% for id in site.data.idDefault %}
- Description of the **{{ id.nameOfTheID }}** id:
  {{ id.description }}.
{% endfor %}

###Pay attention!
In the html file `indexDefault.html` there are **link** tags. The `<link rel="stylesheet" href="styleDefault.css">` link tag is link to an external style sheet `styleDefault.css`. Both files, the html file and the css file, you can find in our [GitHub](https://github.com/EilonBenIshay/PolicyModelsProjectFrontend2022). The other link tags are necessary for the font of the text in the interview.

```yaml
<head>
    <title>Document</title>
    <link rel="stylesheet" href="styleDefault.css">
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Nunito&display=swap" rel="stylesheet">
</head>
<body style="font-family: 'Nunito', sans-serif">
    <h4>This is a site that wanted the default PolicyModels web-component embedded</h4>
    <policy-models-default name="PolicyModels">
        <div id="style">styleDefault.css</div>
        <div id="model">WORKRIGHTS</div>
    </policy-models-default>
    <script src="policyModelsDefault.js"></script>
</body>
```

## "Chat" web component

