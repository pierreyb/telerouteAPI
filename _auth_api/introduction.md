---
title: Introduction
position_number: 1
parameters:
  - name:
    content:
content_markdown: >-
  The access token is valid only for a limited time, indicated by the expiration
  time in the response attribute 'expires\_in'. Obtaining an Access Token is
  done via POST method, passing token parameters via the URL.


request_code_block:
  - code_block:
    title: Endpoint
    
response_code_blocks:
    title: ENDPOINTS
    endpoints:
      - method: POST
        resource: /user/token
---