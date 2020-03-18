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


endpoint_block:
    title: ENDPOINTS
    endpoints:
      - method: post
        resource: /user/token
---