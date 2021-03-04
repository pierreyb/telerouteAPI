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
  * freight description type
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

      --header 'Accept-Version: v2' \

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
                "start": "2020-04-24T10:00:00",
                "end": "2020-04-24T18:00:00"
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
  - code_block: |-
      {
          "header": {
              "statusCode": 201,
              "timestamp": "2020-03-18T17:13:37+01:00",
              "login": "userlog",
              "request": "POST https://{url}/freight/offers",
              "version": "v1"
          },
          "errors": [],
          "warnings": [],
          "content": {
              "offerId": "4tkn0m72ioh1n",
              "externalId": "4tkn0m72ioh1n",
              "paymentDue": 30,
              "pickUp": {
                  "location": {
                      "address": {
                          "country": "BE",
                          "city": "Ixelles",
                          "zip": "1050"
                      },
                      "regions": []
                  },
                  "interval": {
                      "start": "2020-04-24T11:00:00",
                      "end": "2020-04-24T19:00:00",
                      "empty": false
                  }
              },
              "delivery": {
                  "location": {
                      "address": {
                          "country": "ES",
                          "city": "Barcelona",
                          "zip": "08"
                      },
                      "regions": []
                  },
                  "interval": {
                      "empty": true
                  }
              },
              "freightDescription": {
                  "type": "GENERAL_MERCHANDISE",
                  "netWeight": 24.000,
                  "length": 13.000,
                  "hazardousness": {
                      "hazardous": false
                  },
                  "temperatureControlled": false,
                  "transportPackage": {
                      "exchangeable": false
                  },
                  "hazardous": false,
                  "requiredVehicles": [
                      "TAUTLINER"
                  ]
              },
              "addInfo": {
                  "comment": "Comment"
              },
              "company": {
                  "id": "xxxx",
                  "name": "Your company",
                  "country": "BE",
                  "profileLink": "https://cdhost/AdminModule.html?redirect=community/cd_details/xxx"
              },
              "contact": {
                  "fullName": "PACO Y YOLANDA                                              ",
                  "phoneNumber": "+34 976000000",
                  "faxNumber": "+34 976844107",
                  "email": "trash@wtransnet.com",
                  "language": "en_US"
              },
              "targetPrice": {
                  "currency": "EUR",
                  "visibility": false
              },
              "owner": {
                  "login": "userlogin"
              },
              "offerStatus": "ACTIVE",
              "uplifts": 3,
              "viewers": 0,
              "posted": "2020-03-18T17:13:37+01:00",
              "updated": "2020-03-18T17:13:37+01:00",
              "contactLanguage": "en_US",
              "links": [
                  {
                      "rel": "self",
                      "href": "https://api.fx.wktransportservices.com/freight/offers/4tkn0m72ioh1n"
                  }
              ]
          }
      }
    title: Response body
    language: javascript
---