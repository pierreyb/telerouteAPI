---
title: /vehicle/offers
position_number: 2
type: post
description: Create a vehicle offer
parameters:
  - name:
    content:
content_markdown: |-
  In order to create a new vehicle, the following information is mandatory:

  * departure address
  * departure interval start date (time is optional)
  * arrival address
  * vehicle type
  * owner login
left_code_blocks:
  - code_block:
    title:
    language:
right_code_blocks:
  - code_block: "curl --location --request POST 'https://api.fx.wktransportservices.com/vehicle/offers' \\\n--header 'Authorization: Bearer eyJh...' \\\n--header 'Content-Type: application/json' \\\n--header 'Accept-Version: v2' \\\n--data-raw '{\n  \"departure\": {\n    \"location\": {\n      \"address\": {\n        \"country\": \"ES\",\n        \"city\": \"Terrassa\",\n        \"zip\": \"08225\"\n      }\n    },\n    \"interval\": {\n      \"start\": \"2019-12-09T08:00:00\",\n      \"end\": \"2019-12-09T20:00:00\"\n    }\n  },\n  \"arrival\": {\n    \"location\": {\n      \"address\": {\n        \"country\": \"ES\",\n        \"city\": \"Manresa\",\n        \"zip\": \"08241\"\n      }\n    },\n    \"interval\": {\n      \"start\": \"2019-12-09T08:00:00\",\n      \"end\": \"2019-12-10T20:00:00\"\n    }\n  },\n  \"loadDescription\": {\n    \"vehicle\": \"TAUTLINER\",\n    \"weight\": 24,\n    \"length\": 13.6,\n    \"volume\": 12.1\n  },\n  \"owner\": {\n  \t\"login\": \"username\"\n  },\n\n  \"addInfo\": {\n    \"comment\": \"This is a comment\"\n  }\n    \n}"
    title: Request example
    language: bash
  - code_block: "{\r\n    \"header\": {\r\n        \"statusCode\": 201,\r\n        \"timestamp\": \"2020-03-18T17:13:37+01:00\",\r\n        \"login\": \"userlog\",\r\n        \"request\": \"POST https://{url}/vehicle/offers\",\r\n        \"version\": \"v1\"\r\n    },\r\n    \"errors\": [],\r\n    \"warnings\": [],\r\n    \"content\": {\r\n        \"offerId\": \"4tkn0m72ioh1n\",\r\n        \"externalId\": \"4tkn0m72ioh1n\",\r\n        \"paymentDue\": 30,\r\n        \"pickUp\": {\r\n            \"location\": {\r\n                \"address\": {\r\n                    \"country\": \"BE\",\r\n                    \"city\": \"Ixelles\",\r\n                    \"zip\": \"1050\"\r\n                },\r\n                \"regions\": []\r\n            },\r\n            \"interval\": {\r\n                \"start\": \"2020-04-24T11:00:00+02:00\",\r\n                \"end\": \"2020-04-24T19:00:00+02:00\",\r\n                \"empty\": false\r\n            }\r\n        },\r\n        \"delivery\": {\r\n            \"location\": {\r\n                \"address\": {\r\n                    \"country\": \"ES\",\r\n                    \"city\": \"Barcelona\",\r\n                    \"zip\": \"08\"\r\n                },\r\n                \"regions\": []\r\n            },\r\n            \"interval\": {\r\n                \"empty\": true\r\n            }\r\n        },\r\n        \"vehicleDescription\": {\r\n            \"type\": \"GENERAL_MERCHANDISE\",\r\n            \"netWeight\": 24.000,\r\n            \"length\": 13.000,\r\n            \"hazardousness\": {\r\n                \"hazardous\": false\r\n            },\r\n            \"temperatureControlled\": false,\r\n            \"transportPackage\": {\r\n                \"exchangeable\": false\r\n            },\r\n            \"hazardous\": false,\r\n            \"requiredVehicles\": [\r\n                \"TAUTLINER\"\r\n            ]\r\n        },\r\n        \"addInfo\": {\r\n            \"comment\": \"Comment\"\r\n        },\r\n        \"company\": {\r\n            \"id\": \"xxxx\",\r\n            \"name\": \"Your company\",\r\n            \"country\": \"BE\",\r\n            \"profileLink\": \"https://cdhost/AdminModule.html?redirect=community/cd_details/xxx\"\r\n        },\r\n        \"contact\": {\r\n            \"fullName\": \"PACO Y YOLANDA                                              \",\r\n            \"phoneNumber\": \"+34 976000000\",\r\n            \"faxNumber\": \"+34 976844107\",\r\n            \"email\": \"trash@wtransnet.com\",\r\n            \"language\": \"en_US\"\r\n        },\r\n        \"targetPrice\": {\r\n            \"currency\": \"EUR\",\r\n            \"visibility\": false\r\n        },\r\n        \"owner\": {\r\n            \"login\": \"userlogin\"\r\n        },\r\n        \"offerStatus\": \"ACTIVE\",\r\n        \"uplifts\": 3,\r\n        \"viewers\": 0,\r\n        \"posted\": \"2020-03-18T17:13:37+01:00\",\r\n        \"updated\": \"2020-03-18T17:13:37+01:00\",\r\n        \"contactLanguage\": \"en_US\",\r\n        \"links\": [\r\n            {\r\n                \"rel\": \"self\",\r\n                \"href\": \"https://api.fx.wktransportservices.com/vehicle/offers/4tkn0m72ioh1n\"\r\n            }\r\n        ]\r\n    }\r\n}"
    title: Response body
    language: javascript
---