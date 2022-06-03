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
There are two web components:

The first web component,**"Default" web component**, is the default interview constructed as follows- multiple choice questions that can be answered by clicking a button that represents the appropriate answer. 

The second web component,**"Chat" web component**, is in the form of a chat where you can answer questions using two ways: the first way is by clicking on a button that represents the appropriate answer and the second way is to type in the text box the appropriate answer number. 

### How it looks like...

#### The "Default" web component

<img width="335" alt="צילום מסך של האתר" src="<img width="678" alt="defaultInterview" src="https://user-images.githubusercontent.com/48415128/171925369-276bbf17-c570-4505-aa02-4a9f49fccd74.png">

#### The "Chat" web component

<img width="335" alt="צילום מסך של האתר" src="https://user-images.githubusercontent.com/48415128/158069121-13250618-4f39-468d-a442-c9198fc3e6c8.png">

### Pay attention
All the following steps are done in your **html file**.


### 1. Quick start: Use a Html tag


In the **_body_** tag on your html page, add a html tag that called _policy-models-default_ or _policy-models-Chat_.

>In case of **_policy-models-default_** it will be like this: 

```yaml
<policy-models-default name="PolicyModels">
    </policy-models-default>
```
>In case of **_policy-models-Chat_** it will be like this: 

```yaml
<policy-models-Chat name="PolicyModels">
    </policy-models-Chat>
```

<small> There is an attribute "name" that specifies the name of the element. In our case it is _PolicyModels_.
    
   
### 2. Add Model
    

In the html **_policy-models-default_** tag or **_policy-models-Chat_** tag add:
    
```yaml
 <div id="model"> <<nameOfModel>> </div>
```
    
In the **<<nameOfModel>>** you need to write the **name of the model** of the interview. 
If you have selected a non-existent interview model, an error message will appear.
    
    
### 3. Add Style
    

In the html **_policy-models-default_** tag or **_policy-models-Chat_** tag add:
    
```yaml
 <div id="style"> <<nameOfFile>> </div>
```
    
In the **<<nameOfFile>>** you need to write the **name of the css file** that describes the style that you want the site to have.
    

    You can find our css file in our [GitHub](https://github.com/EilonBenIshay/PolicyModelsProjectFrontend2022). 
    
**Pay Attention!** You need to put the css file in the same folder as the html file.
    
>In case of **_policy-models-default_** it will be like this: `style.css`
    
```yaml
    <div id="style">style.css</div>
```
    
>In case of **_policy-models-Chat_** it will be like this: `styleChat.css`
    
```yaml
    <div id="style">styleChat.css</div>
```
    
## [How to write the css file](https://shellytalis.github.io/policy-model-tutorial/style.html)
    
    
    
### 4. Add Script tag
    
    
In the **_body_** tag on your html page, after the _policy-models-default_ tag, add a html tag that called **_script_**. There is an attribute _src_ that specifies the source of the java script file.

```yaml
    <script src= <<nameOfFile>> ></script>
```
    
In the **_<<nameOfFile>>_** you need to write the **name of the source file**. 
    

    You can find our source file in our [GitHub](https://github.com/EilonBenIshay/PolicyModelsProjectFrontend2022). 
    
**Pay Attention!** You need to put the js file in the same folder as the html file.
    
>In case of **_policy-models-default_** it will be like this: `policyModelsDefault.js`
    
```yaml
    <script src="policyModelsDefault.js"></script>
```
    
>In case of **_policy-models-Chat_** it will be like this: `policyModelsChat.js`
    
```yaml
    <script src="policyModelsChat.js"></script>
```
    
    
### Finally 
    
    
After all the steps, the html file should looking like this:
    
```yaml
    <html>
    <body>
        <policy-models-Chat name="PolicyModels">
            <div id="style">styleChat2.css</div>
            <div id="model">WORKRIGHTS</div>
        </policy-models-Chat>
        <script src="policyModelsChat.js"></script>
    </body>
    </html>
```
You can find our full html file `index.html` in our [GitHub](https://github.com/EilonBenIshay/PolicyModelsProjectFrontend2022)
---

## About the project

Policy Models Tutorial is &copy; 2022-{{ "now" | date: "%Y" }} by Shelly, Eilon and Shady.
