---
title: '/freight/offers/:externalId'
position_number: 3
type: put
description: Create or update a freight offer based on an external ID
parameters:
  - name:
    content:
content_markdown: >-
  Update of the offer is referenced via the 'externalId'. When an offer is
  updated, its 'externalId' remains the same while a new 'offerId' will be
  generated
left_code_blocks:
  - code_block:
    title:
    language:
right_code_blocks:
  - code_block: |-
      curl --location --request PUT
            'https://api.fx.wktransportservices.com/freight/offers/aaaasfbf4mgaf' \
            --header 'Authorization: Bearer eyJh...' 
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
          "requiredVehicles": ["TAUTLINER"]
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
---
