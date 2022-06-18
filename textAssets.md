---
layout: default
title: textAssets
nav_order: 3
---
The file `textAssets.js` contains all the text assets for each language of the chosen model (Including but not limited to - the text inside buttons, titles, etc).

Each model has its own languages. 
To add or remove a language, to change the text of a button or title - you **must** modify this file - `textAssets.js`. 

---

### Pay Attention!

Modifying this file is **mandatory**. This file being fully updated is a must for the web component to run at all. 

---

**How to find the languages available for a model?**

Go to any browser of your choice (can also use the commandline with the command 'curl') and type - 
`[serverDomain]/apiInterviewCtrl/${modelId}/start/`. 
Replace the ${modelId} with the Model Id you found before. This shall give you a list of all the possible languages for this specific model. `[serverDomain]` is `https://policymodelsserver.azurewebsites.net/`. 

---

### After finding the languages of the model ... 


In order to **add a Language** you must write the following - 

`TextAssets.set(${languageName}, ${languageObject});`

A language object looks like this (this is an example for English)- 
```json
{
    welcome: "Welcome",
    start_interview: "Start Interview",
    start: "Start",
    show_transcript: "Show Transcript",
    hide_transcript: "Hide Transcript",
    question: "Question",
    your_answer: "Your answer",
    revisit: "Revisit this question",
    show_conclusion: "Show Conclusion",
    home: "Home",
    welcome: "Welcome to the PolicyModels test site!",
    result: "Your results",
    conclusion_page: "Conclusion Page",
    press_conclusions: "Press the \"show conclusion\" button to see the conclusion of your interview",
    download_transcript: "Download Transcript",
    write_feedback: "Write feedback",
    submit_feedback: "submit feedback",
    show_tags: "Show Current Tags (intermediate result)",
    hide_tags: "Hide Current Tags (intermediate result)",
    my_feedback_is: "My Feedback is:",
    my_name_is: "My name is:",
    download_conclusions: "Download Conclusions",
    enter_answer: "Enter your answer here",
    write_comment: "Add personal comment",
    hide_comment: "Hide comment",
    my_comment_is: "my comment is:"
}
```
You can find a more in-depth explanation of what each attribute is down below.

**Note** - every attribute is important and mandatory. Skipping an attribute will result in the WC crashing.

**Pay Attention**, the first language that is added to the map _TextAssets_ is the **default** language. That means it's the language of the interview when it starts. In addition, the conclusions at the end of the interview will be downloaded in this language.

---

### The attributes are:

* 1 - languages - describes the content of the options in the languages menu.

* 2 - welcome^^ - describes the content of the title on the welcome page

* 3 - start_interview - describes the content of the button 

* 4 - start - describes the content of the button 

* 5 - enter_answer^^ - describes the content of the placeholder of the input

* 6 - show_transcript^ - describes the content of the button 

* 7 - hide_transcript^ - describes the content of the button 

* 8 - question^ - describes the content in the transcript

* 9 - your_answer^ - describes the content in the transcript

* 10 - revisit - describes the content of the button 

* 11 - show_conclusion - describes the content of the button 

* 12 - home - describes the content of the button 

* 13 - welcome_PM^ - describes the content of the title

* 14 - results - describes the content on the conclusion page

* 15 - conclusion_page - describes the content of the title on the conclusion page

* 16 - press_conclusions - describes the content that appears after the last question

* 17 - download_transcript - describes the content of the button 

* 18 - download_conclusions - describes the content of the button 

* 19 - write_feedback - describes the content of the button 

* 20 - submit_feedback - describes the content of the button 

* 21 - show_tags - describes the content of the button 

* 22 - hide_tags - describes the content of the button 

* 23 - my_feedback_is - describes the content of the placeholder of the input 

* 24 - my_name_is - describes the content of the placeholder of the input 

* 25 - write_comment - describes the content of the button 

* 26 - submit_comment - describes the content of the button 

* 27 - my_comment_is - describes the content of the placeholder of the input 

--- 

Attached below are photos of the course of the interview. In each image, the attribute is surrounded by its number.

Note - Some attributes appear in only one web component.

^only relevant for default WC
^^only relevant for Chat WC

---

### In case of *"Default"* web component

----

<img width="651" alt="default1" src="https://user-images.githubusercontent.com/48415128/173601935-2401161b-2c85-494a-b519-be1af79a76f1.png">

----

<img width="651" alt="default2" src="https://user-images.githubusercontent.com/48415128/173602041-15d16baa-7a06-468e-a630-6554a79810fc.png">

----

<img width="651" alt="default3" src="https://user-images.githubusercontent.com/48415128/173602121-b2b2846a-df1e-4478-b656-f329d2925c68.png">

----

<img width="651" alt="default4" src="https://user-images.githubusercontent.com/48415128/173602209-296ba97f-12b9-4588-8896-88a2428c9102.png">

----

<img width="651" alt="default5" src="https://user-images.githubusercontent.com/48415128/173602280-be353f0c-7006-4fbd-af5f-68a32c2946ff.jpeg">


### In case of *"Chat"* web component

----

<img width="651" alt="chat1" src="https://user-images.githubusercontent.com/48415128/173581010-2c68e79f-12a9-49a0-9667-0f5c2c27c65b.png">

----

<img width="651" alt="chat2" src="https://user-images.githubusercontent.com/48415128/173581251-786cae5a-9588-477e-a391-169e264f4748.png">

----

<img width="651" alt="chat3" src="https://user-images.githubusercontent.com/48415128/173581314-61910e6f-8e13-40dc-a8b0-90a7e427c9df.png">

----

<img width="651" alt="chat5" src="https://user-images.githubusercontent.com/48415128/173581396-e88cdd69-b1b9-4cac-8c8a-3d5536c94ccb.png">

----

<img width="651" alt="chat5" src="https://user-images.githubusercontent.com/48415128/173581731-d5b16fc7-06e3-415c-aa28-79e2f901c164.png">

