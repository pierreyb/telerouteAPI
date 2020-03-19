---
title: '/freight/offer-detail/:offerId'
position_number: 9
type: get
description: Retrieve the detail of a freight offer with the contact information
parameters:
  - name:
    content:
content_markdown:
left_code_blocks:
  - code_block:
    title:
    language:
right_code_blocks:
  - code_block: "curl --location --request GET 'https://api.fx.wktransportservices.com/freight/offer-detail/cs5adp2piq7ongaple' \\\r\n--header 'Authorization: Bearer eyJh...'"
    title: Request example
    language: bash
  - code_block: "{\r\n    \"header\": {\r\n        \"statusCode\": 200,\r\n        \"timestamp\": \"2020-03-19T16:03:29+01:00\",\r\n        \"login\": \"userLogin\",\r\n        \"request\": \"GET https://api.mkt.sprint.alpega.info/freight/offer-detail/cs5adp2piq7ongaple\",\r\n        \"version\": \"v1\"\r\n    },\r\n    \"errors\": [],\r\n    \"warnings\": [],\r\n    \"content\": {\r\n        \"pickup\": {\r\n            \"country\": \"FR\",\r\n            \"city\": \"Paris\",\r\n            \"postalCode\": \"75001\",\r\n            \"coordinates\": {\r\n                \"longitude\": 2.33896,\r\n                \"latitude\": 48.86278\r\n            }\r\n        },\r\n        \"delivery\": {\r\n            \"country\": \"FR\",\r\n            \"city\": \"Bordeaux\",\r\n            \"postalCode\": \"33***\",\r\n            \"coordinates\": {\r\n                \"longitude\": -0.58097,\r\n                \"latitude\": 44.83664\r\n            }\r\n        },\r\n        \"company\": {\r\n            \"id\": \"xxx\",\r\n            \"name\": \"Company name\",\r\n            \"country\": \"FR\",\r\n            \"profileLink\": \"https://cdhost/AdminModule.html?redirect=community/cd_details/xxx\"\r\n        },\r\n        \"contact\": {\r\n            \"fullName\": \"contact name\",\r\n            \"preferedLanguage\": \"en_US\",\r\n            \"phone\": \"+3212312312\",\r\n            \"email\": \"info@teleroute.com\"\r\n        },\r\n        \"freightDescription\": {\r\n            \"type\": \"CONTAINER\",\r\n            \"netWeight\": 15.0,\r\n            \"length\": 11.0,\r\n            \"hazardousness\": {\r\n                \"hazardous\": false\r\n            },\r\n            \"temperatureControlled\": false,\r\n            \"requiredVehicles\": [],\r\n            \"palletExchange\": false,\r\n            \"gmpCertificate\": false,\r\n            \"requiredEquipment\": []\r\n        },\r\n        \"paymentTerm\": 30,\r\n        \"endDate\": {},\r\n        \"startDate\": {\r\n            \"start\": \"2020-03-19 00:00:00\"\r\n        },\r\n        \"routeDetails\": {\r\n            \"distance\": 585,\r\n            \"travelTime\": 470\r\n        },\r\n        \"externalId\": \"1lrjr94kq58fv\",\r\n        \"offerId\": \"cs5adp2piq7ongaple\",\r\n        \"posted\": \"2020-03-19T14:29:40+01:00\"\r\n    }\r\n}"
    title: Response body
    language: javascript
---
