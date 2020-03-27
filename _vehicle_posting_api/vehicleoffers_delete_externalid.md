---
title: '/vehicle/offers/:externalId'
position_number: 4
type: delete
description: Delete a vehicle offer based on an external ID
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
            'https://api.fx.wktransportservices.com/vehicle/offers/aaaasfbf4mgaf' \
            --header 'Authorization: Bearer eyJh...' \
            --header 'Accept-Version: “v1”' 
    title: Request example
    language: bash
---
