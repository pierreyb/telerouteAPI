---
title: /oauth/token
position_number: 2
type: put
description: Generate a bearer token
parameters:
  - name: client_id
    content: 'Application Id. Fixed value : "freightexchange"'
  - name: client_secret
    content: 'Fixed value : "secret"'
  - name: scope
    content: 'The scopes which you want to request authorization for. Value : "any"'
  - name: grant_type
    content: 'Type of token you apply for. Fixed Value : "password"'
  - name: username
    content: User application username.
  - name: password
    content: User application password.
content_markdown: >-
  The response object


  | **Key** | **Value** | **Description** |
  
  | --- | --- | --- |

  | access\_token | &nbsp; | JSON Web Token |

  | token\_type | Bearer |
  [https://oauth.net/2/bearer-tokens/](https://oauth.net/2/bearer-tokens/) |

  | refresh\_token | &nbsp; | JSON Web Token |

  | expires\_in | 3599 | Expiration time, expressed in seconds (Unix time stamp)
  |

  | scope | any | &nbsp; |

  | user.fname | &nbsp; | User First Name |

  | user.a\_uplft\_init | &nbsp; | Initial counter for Auto uplift feature.
  Default value set to 1. |

  | user.cmp\_post\_code | &nbsp; | User Company Postal Code |

  | user.login | &nbsp; | User Application Login |

  | user.cmp\_name | &nbsp; | User Company Name |

  | user.lname | &nbsp; | User Last Name |

  | user.phone | &nbsp; | User Phone Number |

  | user.a\_uplft\_cnt | &nbsp; | Max Number of Auto uplifts allowed for user |

  | user.id | &nbsp; | User Unique Application Identifier |

  | user.bus\_id | &nbsp; | User Business Identifier |

  | user.fax | &nbsp; | User Fax Number |

  | user.lang | &nbsp; | User Interface Language |

  | user.email | &nbsp; | User Email Address |

  | user.sp\_langs | &nbsp; | User Spoken Languages |

  | user.a\_uplft | &nbsp; | Auto uplift enabled for user. 1 = true, 0 = false.   |

  | jti | &nbsp; | JWT id |

  &nbsp;
left_code_blocks:
  - code_block: "{\r\n    \"access_token\": \"eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJ1c2…\",\r\n    \"token_type\": \"bearer\",\r\n    \"refresh_token\": \"eyJhbGciOiJIUzI1NiIsInR5cCI6IkpX… \",\r\n    \"expires_in\": 3599,\r\n    \"scope\": \"any\",\r\n    \"user\": {\r\n        \"fname\": \"FirstName\",\r\n        \"a_uplft_init\": \"1\",\r\n        \"cmp_post_code\": \"1930\",\r\n        \"login\": \"userlogin\",\r\n        \"cmp_name\": \"MyCompany\",\r\n        \"cmp_id\": \"123456789\",\r\n        \"lname\": \"LastName\",\r\n        \"phone\": \"+3221234567\",\r\n        \"a_uplft_cnt\": \"3\",\r\n        \"id\": \"0001\",\r\n        \"bus_id\": \"abc-123456\",\r\n        \"fax\": null,\r\n        \"lang\": \"en_GB\",\r\n        \"email\": \"someone@transwide.com\",\r\n        \"sp_langs\": [],\r\n        \"a_uplft\": \"1\"\r\n    },\r\n    \"jti\": \"26334f53-c148-45a4-bfd7-71cfb45aeb7e\"\r\n}\r\n"
    title: Response
    language: javascript
right_code_blocks:
  - code_block: >
      curl -X POST \

      'https://api.fx.demo.wktransportservices.com/oauth/token?client_id=freightexchange&client_secret=secret&scope=any&grant_type=password&username={username}&password={password}'
      \
        -H 'Accept: application/json' \
        -H 'Cache-Control: no-cache' \
    title: Request bearer token
    language: bash
---

