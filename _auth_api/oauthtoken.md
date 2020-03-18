---
title: /oauth/token
position_number: 2
type: put
description: Generate a bearer token
parameters:
  - name: client_id
    content: 'Application Id. Fixed value : "freightexchange"'
  - name: client_secret
    content: 'Fixed value : "secret"'
  - name: scope
    content: 'The scopes which you want to request authorization for. Value : "any"'
  - name: grant_type
    content: 'Type of token you apply for. Fixed Value : "password"'
  - name: username
    content: User application username.
  - name: password
    content: User application password.
content_markdown: >-
  The response object


  | **Key** | **Value** | **Description** |
  
  | --- | --- | --- |

  | access\_token | &nbsp; | JSON Web Token |


left_code_blocks:
  - code_block: "{\r\n    \"access_token\": \"eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJ1c2…\",\r\n    \"token_type\": \"bearer\",\r\n    \"refresh_token\": \"eyJhbGciOiJIUzI1NiIsInR5cCI6IkpX… \",\r\n    \"expires_in\": 3599,\r\n    \"scope\": \"any\",\r\n    \"user\": {\r\n        \"fname\": \"FirstName\",\r\n        \"a_uplft_init\": \"1\",\r\n        \"cmp_post_code\": \"1930\",\r\n        \"login\": \"userlogin\",\r\n        \"cmp_name\": \"MyCompany\",\r\n        \"cmp_id\": \"123456789\",\r\n        \"lname\": \"LastName\",\r\n        \"phone\": \"+3221234567\",\r\n        \"a_uplft_cnt\": \"3\",\r\n        \"id\": \"0001\",\r\n        \"bus_id\": \"abc-123456\",\r\n        \"fax\": null,\r\n        \"lang\": \"en_GB\",\r\n        \"email\": \"someone@transwide.com\",\r\n        \"sp_langs\": [],\r\n        \"a_uplft\": \"1\"\r\n    },\r\n    \"jti\": \"26334f53-c148-45a4-bfd7-71cfb45aeb7e\"\r\n}\r\n"
    title: Response
    language: javascript
right_code_blocks:
  - code_block: >
      curl -X POST \

      'https://api.fx.demo.wktransportservices.com/oauth/token?client_id=freightexchange&client_secret=secret&scope=any&grant_type=password&username={username}&password={password}'
      \
        -H 'Accept: application/json' \
        -H 'Cache-Control: no-cache' \
    title: Request bearer token
    language: bash
---

