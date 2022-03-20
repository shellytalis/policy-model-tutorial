---
layout: default
title: Home
nav_order: 1
description: "Policy Models Tutorial."
permalink: /
---

# Policy Models Tutorial
{: .fs-9 }

A documentation about Policy Models web component
{: .fs-6 .fw-300 }

[Get started now](#getting-started){: .btn .btn-primary .fs-5 .mb-4 .mb-md-0 .mr-2 } [View it on GitHub](https://github.com/EilonBenIshay/PolicyModelsProjectFrontend2022){: .btn .fs-5 .mb-4 .mb-md-0 }

---

## Getting started

### How it looks like...

<img width="335" alt="צילום מסך של האתר" src="https://user-images.githubusercontent.com/48415128/158069121-13250618-4f39-468d-a442-c9198fc3e6c8.png">

### Quick start: Use a Html tag

1. In the _body_ tag on your html page, add a html tag that called _policy-models-default_ like this:

```yaml
<policy-models-default name="PolicyModels">
    </policy-models-default>
```

<small> There is an attribute "name" that specifies the name of the element. In our case it is PolicyModels.
    
2. In the _body_ tag on your html page, after the _policy-models-default_ tag, add a html tag that called _script_. There is an attribute _src_ that specifies the source of the java script file.

```yaml
    <script src= <<nameOfFile>> ></script>
```
    
<small> In the _<<nameOfFile>>_ you need to write the name of the source file. For example, if the name of the file is `app.js` that it will be like this: 
    
```yaml
    <script src="app.js"></script>
```
    
### Add Style

1. In the html tag _policy-models-default_ add:
    
```yaml
 <div id="style"> <<nameOfFile>> </div>
```
    
<small> In the _<<nameOfFile>>_ you need to write the name of the css file that describes the style that you want the site to have. For example, if the name of the file is `style.css` that it will be like this: 
    
```yaml
<div id="style">style.css</div>
```
    
### [How to write the css file](https://shellytalis.github.io/policy-model-tutorial/style.html)
    


---

## About the project

Policy Models Tutorial is &copy; 2022-{{ "now" | date: "%Y" }} by Shelly, Eilon and Shady.
