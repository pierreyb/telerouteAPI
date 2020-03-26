---
title: Errors
position_number: 4
parameters:
  - name:
    content:
content_markdown: >-
  The freight exchange uses conventional HTTP response codes to indicate the
  success or failure of an API request.


  In general:


  * Codes in the `2xx` range indicate success.

  * Codes in the `4xx` range indicate an error with the error 
  information provided (e.g., a required parameter was omitted.).

  * Codes in the `5xx` range indicate an error with Teleroute's servers.
  

  &nbsp;


  | Code | Name | Description |

  | --- | --- | --- |

  | 200 | OK | Successful operation |

  | 201 | Created | Resource is successfully added |

  | 400 | Bad Request | Malformed request or missing parameters |

  | 401 | Unauthorized | Authentication failed. Invalid token. |

  | 403 | Forbidden | No permission to this resource. |

  | 404 | Not Found | The specified resource is not found or does not exist |

  | 405 | Method Not Allowed | Method is not allowed or not implemented on this
  endpoint |

  | 500 | Internal Server Error | Server problem or bad request that cannot be
  parsed |
right_code_blocks:
  - code_block:
    title:
    language:
---