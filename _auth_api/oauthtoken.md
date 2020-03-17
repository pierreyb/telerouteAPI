---
title: /oauth/token
position_number: 2
type: put
description: generate a bearer token
parameters:
  - name: client_id
    content: freightexchange
  - name: client_secret
    content: secret
  - name: scope
    content: any
  - name: grant_type
    content: password
  - name: username
    content:
      username:
  - name: password
    content:
      password:
content_markdown: >-
  The access token is valid only for a limited time, indicated by the expiration
  time in the response attribute 'expires\_in'.


  Obtaining an Access Token is done via POST method, passing token parameters
  via the URL.
left_code_blocks:
  - code_block:
    title:
    language:
right_code_blocks:
  - code_block:
    title:
    language:
---

