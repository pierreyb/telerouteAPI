---
title: '/freight/offers/:externalId'
position_number: 5
type: delete
description: Delete a freight offer based on an external ID
parameters:
  - name:
    content:
content_markdown:
left_code_blocks:
  - code_block:
    title:
    language:
right_code_blocks:
  - code_block: |-
      curl --location --request DELETE
            'https://api.fx.wktransportservices.com/freight/offers/aaaasfbf4mgaf' \
            --header 'Authorization: Bearer eyJh...' 
    title: Request example
    language: bash
---
