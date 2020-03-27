---
title: /freight/searches
position_number: 2
type: post
description: Create a new search for freight
parameters:
  - name:
    content:
content_markdown: >-
  In order to create a new search for freight, the following information is
  mandatory:


  * a departure or an arrival

  * owner


  The departure and arrival information can be


  * either a city with a search radius

  * either a list of region
left_code_blocks:
  - code_block:
    title:
    language:
right_code_blocks:
  - code_block: "curl --location --request POST 'https://api.mkt.sprint.alpega.info/freight/searches' \\\n--header 'Authorization: Bearer eyJh...' \\\n--header 'Accept-Version: “v1”' \\\n--header 'Content-Type: application/json' \\\n--data-raw '{\n  \"departure\": {\n      \"address\": {\n      \t\"country\": \"BE\",\n      \t\"city\": \"Bruxelles\",\n      \t\"radius\" : 100\n      }\n  },\n  \"arrival\": {\n      \"regions\": [\n        \"IT\",\n        \"FR-75\"\n      ]\n  },\n  \"loadingInterval\": {\n    \"loadingTime\": \"NO_DATE\",\n    \"start\": \"2020-01-17\"\n  },\n  \"loadDescription\": {\n\t\"goods\": \"GENERAL_MERCHANDISE\",\n    \"weight\": {\n      \"min\": 0,\n      \"max\": 999\n    },\n    \"length\": {\n      \"min\": 0,\n      \"max\": 25\n    },\n    \"volume\": {\n      \"min\": 0,\n      \"max\": 999\n    },\n    \"temperatureControlled\": false,\n    \"hazardous\": false,\n    \"vehicles\": []\n  },\n  \"owner\": {\n    \"login\": \"userLogin\"\n  }\n}'"
    title: Request example
    language: bash
  - code_block: "{\r\n    \"header\": {\r\n        \"statusCode\": 201,\r\n        \"timestamp\": \"2020-03-19T14:26:55+01:00\",\r\n        \"login\": \"userLogin\",\r\n        \"request\": \"POST https://api.fx.wktransportservices.com/freight/searches\",\r\n        \"version\": \"v1\"\r\n    },\r\n    \"errors\": [],\r\n    \"warnings\": [],\r\n    \"content\": {\r\n        \"searchId\": 190964,\r\n        \"state\": \"ACTIVE\",\r\n        \"title\": \"B Bruxelles - I-IT;F-75\",\r\n        \"departure\": {\r\n            \"address\": {\r\n                \"country\": \"BE\",\r\n                \"city\": \"Bruxelles\",\r\n                \"radius\": 100,\r\n                \"coordinates\": {\r\n                    \"longitude\": 4.3601,\r\n                    \"latitude\": 50.84607\r\n                }\r\n            },\r\n            \"regions\": []\r\n        },\r\n        \"arrival\": {\r\n            \"regions\": [\r\n                \"IT\",\r\n                \"FR-75\"\r\n            ]\r\n        },\r\n        \"loadingInterval\": {\r\n            \"loadingTime\": \"NO_DATE\",\r\n            \"start\": \"2020-03-19\"\r\n        },\r\n        \"searchOptions\": {\r\n            \"extendedSearch\": false,\r\n            \"vehicleDetails\": {\r\n                \"publishVehicle\": false\r\n            }\r\n        },\r\n        \"loadDescription\": {\r\n            \"goods\": \"ALL\",\r\n            \"weight\": {\r\n                \"min\": 0.0,\r\n                \"max\": 999.0\r\n            },\r\n            \"length\": {\r\n                \"min\": 0.0,\r\n                \"max\": 25.0\r\n            },\r\n            \"volume\": {\r\n                \"min\": 0.0,\r\n                \"max\": 999.0\r\n            },\r\n            \"temperatureControlled\": false,\r\n            \"hazardous\": false,\r\n            \"vehicles\": []\r\n        },\r\n        \"owner\": {\r\n            \"login\": \"userlogin\"\r\n        },\r\n        \"posted\": \"2020-03-19T14:26:55+01:00\",\r\n        \"updated\": \"2020-03-19T14:26:55+01:00\",\r\n        \"links\": [\r\n            {\r\n                \"rel\": \"self\",\r\n                \"href\": \"https://api.fx.wktransportservices.com/freight/searches/190964\"\r\n            },\r\n            {\r\n                \"rel\": \"searchResults\",\r\n                \"href\": \"https://api.fx.wktransportservices.com/freight/searches/190964/results\"\r\n            }\r\n        ],\r\n        \"publishVehicle\": false\r\n    }\r\n}"
    title: Response body
    language: javascript
---
