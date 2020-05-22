---
title: '/freight/offers/:offerId'
position_number: 3
type: get
description: Retrieve a freight offer based on an offer ID
parameters:
  - name:
    content:
content_markdown:
left_code_blocks:
  - code_block:
    title:
    language:
right_code_blocks:
  - code_block: |
      curl --location --request GET
            'https://api.fx.wktransportservices.com/freight/offers/aaaasfbf4mgaf' \
            --header 'Authorization: Bearer eyJh...' \
            --header 'Accept-Version: v1' 
    title: Request example
    language: bash
---
