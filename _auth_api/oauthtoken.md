---
title: /oauth/token
position_number: 2
type: put
description: Generate a bearer token
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
content_markdown:
left_code_blocks:
  - code_block:
    title:
    language:
right_code_blocks:
  - code_block: "curl -X POST \\\r\n'https://api.fx.demo.wktransportservices.com/oauth/token?client_id=freightexchange&client_secret=secret&scope=any&grant_type=password&username={username}&password={password}' \\\r\n  -H 'Accept: application/json' \\\r\n  -H 'Cache-Control: no-cache' \\\r\n"
    title: Example
    language: bash
---

