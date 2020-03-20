---
title: '/vehicle/offers/:externalId'
position_number: 3
type: put
description: Create or update a vehicle offer based on an external ID
parameters:
  - name:
    content:
content_markdown: >-
  Update of the offer is referenced via the 'externalId'. When an offer is
  updated, its 'externalId' remains the same while a new 'offerId' will be
  generated
left_code_blocks:
  - code_block:
    title:
    language:
right_code_blocks:
  - code_block: |-
      curl --location --request PUT
            'https://api.fx.wktransportservices.com/vehicle/offers/aaaasfbf4mgaf' \
            --header 'Authorization: Bearer eyJh...' 
    title: Request example
    language: bash
---
