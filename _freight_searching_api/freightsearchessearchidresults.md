---
title: '/freight/searches/:searchId/results'
position_number: 8
type: get
description: Retrieve the freight offer matching the characteristics of the search
parameters:
  - name:
    content:
content_markdown:
left_code_blocks:
  - code_block:
    title:
    language:
right_code_blocks:
  - code_block: >-
      curl --location --request POST
      'https://api.fx.wktransportservices.com/freight/searches/123456/results' \

      --header 'Authorization: Bearer eyJh...'

      --header 'Accept-Version: v1' 
    title: Request example
    language: bash
---
