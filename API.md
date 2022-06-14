---
layout: default
title: API
nav_order: 4
---
# Documentation of the api's with examples

API Endpoints

### GET  /apiInterviewCtrl/models/ 

returns -> Json of available models:

_Output example:_

[
  {
    "id": "1",
    "title": "EndWork",
    "versionId": "1"
  },
  {
    "id": "2",
    "title": "RepositoryTagging",
    "versionId": "1"
  },
  {
    "id": "3",
    "title": "RepositorySelection",
    "versionId": "2"
  }
]

### GET  /apiInterviewCtrl/:modelId/start
returns -> list of available languages of the interview model with modelId

_Output example:_

[
  "en-US",
  "English-Raw",
  "ar-IL",
  "he-IL"
]


### GET  /apiInterviewCtrl/:modelId/:versionId/:languageId/start 

returns -> start of interview and get data about the first question

_Output example:_
	
{
  "ssid": "9a8fbde9-7ddc-4cab-8704-67dd6a6decd5",
  "questionId": "0",
  "questionText": "Are you a woman?",
  "Answers": [
    "yes",
    "no"
  ],
  "AnswersInYourLanguage": [
    "yes",
    "no"
  ],
  "finished": "false",
  "tagsInYourLanguage": {
    "Employer's Obligations": [
      "final account",
      "form 161",
      "approving a working period",
      "letter of termination"
    ]
  },
  "tags": {
    "EmployerObligations": [
      "finalAccountSettlement",
      "jobTerminationConfirmation",
      "workPeriodLetter",
      "form161"
    ]
  }
}

### POST /apiInterviewCtrl/answerPost/ 

answers one question and get the next one in the output. This POST API needs json body contains the values of each one of the required params:

uuid : the userId that you get from the previous api output.

modelId : your modelId

versionId : your model version

languageId :  your desired language

reqNodeId : the index of the question that you want to answer(it must be a question that you have arrived to, it can be from 0 to the current questionId)

answerID : the index of the question that you want to answer

_Output example:_

{
  "ssid": "9a8fbde9-7ddc-4cab-8704-67dd6a6decd5",
  "questionId": "1",
  "questionText": "How old are you? ",
  "Answers": [
    "under 67",
    "67 and over"
  ],
  "AnswersInYourLanguage": [
    "under 67",
    "67 and over"
  ],
  "finished": "false",
  "tagsInYourLanguage": {
    "Case details": {
      "sex": "male"
    },
    "Employer's Obligations": [
      "final account",
      "form 161",
      "approving a working period",
      "letter of termination"
    ]
  },
  "tags": {
    "EmployerObligations": [
      "finalAccountSettlement",
      "jobTerminationConfirmation",
      "workPeriodLetter",
      "form161"
    ],
    "Assertions": {
      "Gender": "male"
    }
  }
}


### GET  /apiInterviewCtrl/askHistory/:uuid/:modelId/:versionId/:languageId/:questionId/

Return the current history, and the answers that you have submit, and also returns in the interview back to the question with id is questionId.

_Output example:_

{
  "questionId": "2",
  "questionText": "Are you an Israeli citizen?",
  "Answers": [
    "yes",
    "no"
  ],
  "AnswersInYourLanguage": [
    "yes",
    "no"
  ],
  "answerHistory": [
    {
      "id": "0",
      "questionText": "Are you a woman?",
      "answer": "no"
    },
    {
      "id": "1",
      "questionText": "How old are you? ",
      "answer": "under 67"
    }
  ],
  "finished": "false",
  "tagsInYourLanguage": {
    "Case details": {
      "age group": "Working age",
      "sex": "male"
    },
    "Employer's Obligations": [
      "final account",
      "form 161",
      "approving a working period",
      "letter of termination"
    ]
  },
  "tags": {
    "EmployerObligations": [
      "finalAccountSettlement",
      "jobTerminationConfirmation",
      "workPeriodLetter",
      "form161"
    ],
    "Assertions": {
      "AgeGroup": "workForce",
      "Gender": "male"
    }
  }
}

### GET  /apiInterviewCtrl/getTags/:uuid/:modelId/:versionId/:languageId/

Returns the tags of the interview in specific language.

_Output example:_

{
  "EmployerObligations": [
    "hearing",
    "finalAccountSettlement",
    "jobTerminationConfirmation",
    "workPeriodLetter",
    "priorNotice",
    "form161"
  ],
  "Notices": [
    "severancePayMethod_Varied",
    "priorNoticePeriod_Varied",
    "relativeSeverancePay"
  ],
  "Benefits": {
    "Properties": [
      "severancePay"
    ]
  },
  "Assertions": {
    "EffectiveTerminationType": "severance",
    "Employment": {
      "Type": "direct",
      "Scope": "partial",
      "SalaryUnits": "daily",
      "Duration": "_0_6"
    },
    "AgeGroup": "workForce",
    "LegalStatus": "palestinianWorkPermit",
    "Gender": "male",
    "ReasonForLeaving": "endOfContract"
  }
}


### GET  /apiInterviewCtrl/feedback/:uuid/:modelId/:versionId/:languageId/:reqNodeId/:writer/:comment/

It submit a feedback on a specific question (reqNodeId) , so the admin of the model can see and improve the questions.

_Output example:_

	“feedback sent.”
