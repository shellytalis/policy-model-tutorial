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

* The first web component,**"Default" web component**, is the default interview constructed as follows- multiple choice questions that can be answered by clicking a button that represents the appropriate answer. 

* The second web component,**"Chat" web component**, is in the form of a chat where you can answer questions using two ways: the first way is by clicking on a button that represents the appropriate answer. The second way is to type in the text box the appropriate answer number. 

## How it looks like...

### The "Default" web component

<img width="887" alt="defaultInterviewNew" src="https://user-images.githubusercontent.com/48415128/171956969-c642453d-9a52-47d9-9263-bf56c436e58d.png">

### The "Chat" web component

<img width="851" alt="chatInterviewNew" src="https://user-images.githubusercontent.com/48415128/172172014-da893494-f8fb-4975-aa82-fbdf0d33d8d1.png">

----

### Pay attention
All the following steps are done in your **html file**.

----

### 1. Quick start: Use a Html tag


In the **_body_** tag on your html page, add a html tag that called _policy-models-default_ or _policy-models-Chat_.

> In case of **_policy-models-default_** it will be like this: 

```yaml
<policy-models-default name="PolicyModels">
    </policy-models-default>
```
> In case of **_policy-models-chat_** it will be like this: 

```yaml
<policy-models-chat name="PolicyModels">
    </policy-models-chat>
```

There is an attribute "name" that specifies the name of the element. In our case it is _PolicyModels_.
    
----
    
### 2. Add modelId and versionId
    

In the html **_policy-models-default_** tag or **_policy-models-chat_** tag add:
    
```yaml
 <div id="modelId> ${modelId} </div>
 <div id="versionId"> ${versionId} </div>
```
    
In the **${modelId}** you need to write the **id of the model** of the interview. 
                   
In the **${versionId}** you need to write the **version id of the model** of the interview. 
                    
> **How to find the Model ID and the Model Version?**

> Go to any browser of your choice (can also use the commandline with the command 'curl') and type - `[serverDomain]/apiInterviewCtrl/models/` . This shall give you a list of all models, their names, Id's and versions.                       
                    
----

### 3. Add Style
    

In the html **_policy-models-default_** tag or **_policy-models-chat_** tag add:
    
```yaml
 <div id="style"> ${nameOfFile} </div>
```
    
In the **${nameOfFile}** you need to write the **name of the css file** that describes the style you want the site to have.
    

You can find our css files in our [GitHub](https://github.com/EilonBenIshay/PolicyModelsProjectFrontend2022). 
    
**Pay Attention!** You need to put the css file in the same folder as the html file.
    
> In case of **_policy-models-default_** it will be like this: `styleDefault.css`
    
```yaml
    <div id="style">styleDefault.css</div>
```
    
> In case of **_policy-models-chat_** it will be like this: `styleChat.css`
    
```yaml
    <div id="style">styleChat.css</div>
```
    
## [How to write the css file](https://shellytalis.github.io/policy-model-tutorial/style.html)
    
----    
    
### 4. Add 3 Script tags
    
    
In the **_body_** tag on your html page, after the _policy-models-default_ tag or the _policy-models-chat_ tag, add 3 html tags called **_script_**. The _src_ attribute specifies the source of the javascript file. The _type_ attribute specifies the type of the script.  

You can find our source files in our [GitHub](https://github.com/EilonBenIshay/PolicyModelsProjectFrontend2022). 
    
**Pay Attention!** You need to put the js files in the same folder as the html file.
    
> In case of **_policy-models-default_** it will be like this: `policyModelsDefault.js`, `connection.js`, `textAssets.js`
    
```yaml
    <script type = "module" src="./policyModelsDefault.js"></script>
    <script type = "module" src="./connection.js"></script>
    <script type = "module" src="./textAssets.js"></script>
```
    
> In case of **_policy-models-chat_** it will be like this: `policyModelsChat.js`, `connection.js`, `textAssets.js`
    
```yaml
    <script type = "module" src="./policyModelsChat.js"></script>
    <script type = "module" src="./connection.js"></script>
    <script type = "module" src="./textAssets.js"></script>
```
                                                 
* `policyModelsDefault.js` or `policyModelsChat.js` is the source file of the web component itself.     
                                                 
* ⋅⋅⋅`connection.js` is a file that is responsible for the connection between the server and the web component.⋅⋅
   ⋅⋅⋅**Pay attention!** On the `connection.js` file, you need to change the serverDomain attribute (in line 5) to the domain of the server.⋅⋅                                              

* ⋅⋅⋅``textAssets.js` is a file that saves all the contents in variables, like the content inside a button or titles.⋅⋅ 
  ⋅⋅⋅`It is **critical** to edit this file for the web component to work. For more information, click [here](https://shellytalis.github.io/policy-model-tutorial/textAssets.html).⋅⋅    
    
----

### Finally 
    
    
After all the steps, the html file should look like this:
    
> In case of **_policy-models-default_** it will be like this: `indexDefault.html`
    
```yaml
    <html>
    <body>
        <policy-models-default name="PolicyModels">
            <div id="style">styleDefault.css</div>
            <div id="modelId">1</div>
            <div id="versionId">1</div>
        </policy-models-default>
        <script type = "module" src="./policyModelsDefault.js"></script>
        <script type = "module" src="./connection.js"></script>
        <script type = "module" src="./textAssets.js"></script>
    </body>
    </html>
```
    
> In case of **_policy-models-chat_** it will be like this: `indexChat.html`
    
```yaml
    <html>
    <body>
        <policy-models-chat name="PolicyModels">
            <div id="style">styleChat.css</div>
            <div id="modelId">1</div>
            <div id="versionId">1</div>
        </policy-models-chat>
        <script type = "module" src="policyModelsChat.js"></script>
        <script type = "module" src="./connection.js"></script>
        <script type = "module" src="./textAssets.js"></script>
    </body>
    </html>
```
You can find our html files in our [GitHub](https://github.com/EilonBenIshay/PolicyModelsProjectFrontend2022)
---


    

Policy Models Tutorial is &copy; 2022-{{ "now" | date: "%Y" }} by Shelly Talis, Eilon Ben Ishay and Shady Obeed.
