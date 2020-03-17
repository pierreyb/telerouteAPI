---
title: Errors
position_number: 4
parameters:
  - name:
    content:
content_markdown: >-
  The freight exchange uses conventional HTTP response codes to indicate the
  success or failure of an API request. In general: Codes in the "***2xx***"
  range indicate success. Codes in the "***4xx"***&nbsp;range indicate an error
  that failed given the information provided (e.g., a required parameter was
  omitted.). Codes in the "***5xx***" range indicate an error with Telertoue's
  servers (these are rare).&nbsp;


  | &nbsp; | &nbsp; | &nbsp; |

  | --- | --- | --- |

  | &nbsp; | &nbsp; | &nbsp; |

  | &nbsp; | &nbsp; | &nbsp; |

  | &nbsp; | &nbsp; | &nbsp; |

  | &nbsp; | &nbsp; | &nbsp; |


  All errors will return JSON in the following format:
left_code_blocks:
  - code_block: |-
      {
        "error": true,
        "message": "error message here"
      }
    title: Response
    language: json
right_code_blocks:
  - code_block:
    title:
    language:
---