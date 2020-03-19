---
title: /freight/offers
position_number: 2
type: post
description: Create a freight offer
parameters:
  - name:
    content:
content_markdown: |-
  In order to create a new freight, the following information is mandatory:

  * pickup address
  * pickup interval start date (time is optional)
  * delivery address
  * freight description netWeight
  * freight description length (except for bulk)
  * freight description volume (only for bulk)
  * owner login
left_code_blocks:
  - code_block:
    title:
    language:
right_code_blocks:
  - code_block: >-
      curl --location --request POST
      'https://api.fx.wktransportservices.com/freight/offers' \

      --header 'Authorization: Bearer eyJh...' \

      --header 'Content-Type: application/json' \

      --data-raw '{
        "externalId": "Externalid",
        "pickUp": {
          "location": {
            "address": {
              "country": "BE",
              "zip": "1050",
              "city": "Ixelles"
            }
          },
          "interval": {
                "start": "2020-04-24T10:00:00+01:00",
                "end": "2020-04-24T18:00:00+01:00"
          }
        },
        "delivery": {
          "location": {
            "address": {
              "country": "ES",
              "zip": "08",
              "city": "Barcelona"
            }
          }
        },
        "freightDescription": {
          "type": "GENERAL_MERCHANDISE",
          "netWeight": 24.0,
          "length": 13.0,
          "volume": null,
          "hazardousness": {
            "hazardous": false
          },
          "temperatureControlled": false,
          "requiredVehicles": ["TAUTLINER"],
          "transportPackage": {
            "exchangeable": false
          }
        },
        "owner": {
          "login": "userlogin"
        },
        "addInfo": {
          "comment": "Comment"
        }
      }'
    title: Request example
    language: bash
  - code_block: "{\r\n    \"header\": {\r\n        \"statusCode\": 201,\r\n        \"timestamp\": \"2020-03-18T17:13:37+01:00\",\r\n        \"login\": \"userlog\",\r\n        \"request\": \"POST https://{url}/freight/offers\",\r\n        \"version\": \"v1\"\r\n    },\r\n    \"errors\": [],\r\n    \"warnings\": [],\r\n    \"content\": {\r\n        \"offerId\": \"4tkn0m72ioh1n\",\r\n        \"externalId\": \"4tkn0m72ioh1n\",\r\n        \"paymentDue\": 30,\r\n        \"pickUp\": {\r\n            \"location\": {\r\n                \"address\": {\r\n                    \"country\": \"BE\",\r\n                    \"city\": \"Ixelles\",\r\n                    \"zip\": \"1050\"\r\n                },\r\n                \"regions\": []\r\n            },\r\n            \"interval\": {\r\n                \"start\": \"2020-04-24T11:00:00+02:00\",\r\n                \"end\": \"2020-04-24T19:00:00+02:00\",\r\n                \"empty\": false\r\n            }\r\n        },\r\n        \"delivery\": {\r\n            \"location\": {\r\n                \"address\": {\r\n                    \"country\": \"ES\",\r\n                    \"city\": \"Barcelona\",\r\n                    \"zip\": \"08\"\r\n                },\r\n                \"regions\": []\r\n            },\r\n            \"interval\": {\r\n                \"empty\": true\r\n            }\r\n        },\r\n        \"freightDescription\": {\r\n            \"type\": \"GENERAL_MERCHANDISE\",\r\n            \"netWeight\": 24.000,\r\n            \"length\": 13.000,\r\n            \"hazardousness\": {\r\n                \"hazardous\": false\r\n            },\r\n            \"temperatureControlled\": false,\r\n            \"transportPackage\": {\r\n                \"exchangeable\": false\r\n            },\r\n            \"hazardous\": false,\r\n            \"requiredVehicles\": [\r\n                \"TAUTLINER\"\r\n            ]\r\n        },\r\n        \"addInfo\": {\r\n            \"comment\": \"Comment\"\r\n        },\r\n        \"company\": {\r\n            \"id\": \"xxxx\",\r\n            \"name\": \"Your company\",\r\n            \"country\": \"BE\",\r\n            \"profileLink\": \"https://cdhost/AdminModule.html?redirect=community/cd_details/xxx\"\r\n        },\r\n        \"contact\": {\r\n            \"fullName\": \"PACO Y YOLANDA                                              \",\r\n            \"phoneNumber\": \"+34 976000000\",\r\n            \"faxNumber\": \"+34 976844107\",\r\n            \"email\": \"trash@wtransnet.com\",\r\n            \"language\": \"en_US\"\r\n        },\r\n        \"targetPrice\": {\r\n            \"currency\": \"EUR\",\r\n            \"visibility\": false\r\n        },\r\n        \"owner\": {\r\n            \"login\": \"userlogin\"\r\n        },\r\n        \"offerStatus\": \"ACTIVE\",\r\n        \"uplifts\": 3,\r\n        \"viewers\": 0,\r\n        \"posted\": \"2020-03-18T17:13:37+01:00\",\r\n        \"updated\": \"2020-03-18T17:13:37+01:00\",\r\n        \"contactLanguage\": \"en_US\",\r\n        \"links\": [\r\n            {\r\n                \"rel\": \"self\",\r\n                \"href\": \"https://api.fx.wktransportservices.com/freight/offers/4tkn0m72ioh1n\"\r\n            }\r\n        ]\r\n    }\r\n}"
    title: Response body
    language: javascript
---