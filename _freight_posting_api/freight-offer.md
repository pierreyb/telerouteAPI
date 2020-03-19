---
title: Freight offer
position_number: 1
parameters:
  - name:
    content:
content_markdown: >-
  Freight offer contain the information related to the goods to be transported.
  In the context of the freight exchange application, the freight are goods
  packaged in a indivisible batch and which needs to be moved in from a loading
  place to a delivery place.


  * The route provides the information about the city where the goods needs to
  be picked up, the city where the goods needs to be delivered and the loading
  date. The delivery date can also be indicates.

  * The freight description provides the information about the goods and
  eventually specification regarding the truck. Goods type will have an impact
  on the type of truck required for the transport, the dimension, the transport
  package and the required certificates for the transportation).


  ##### The freight offer model





  | FreighLocation | L | Description | Type | Length | Cardinality | Constraint
  | Comment |

  | --- | --- | --- | --- | --- | --- | --- | --- |

  | address | 1 | City | String | &nbsp; | 0\..1 | &nbsp; | &nbsp; |

  | country | 2 | Country code | String | 2 | 1 | &nbsp; | &nbsp; |

  | city | 2 | City | String | &nbsp; | 1 | &nbsp; | &nbsp; |

  | zip | 2 | &nbsp; | String | &nbsp; | 0\..1 | &nbsp; | &nbsp; |

  | coordinates | 2 | &nbsp; | &nbsp; | &nbsp; | 0\..1 | Read-Only | &nbsp; |

  | latitude | 3 | &nbsp; | Float | &nbsp; | 1 | between -90 and +90 | &nbsp; |

  | longitude | 3 | &nbsp; | Float | &nbsp; | 1 | between -180 and 180 | &nbsp;
  |

  | interval | 1 | &nbsp; | &nbsp; | &nbsp; | &nbsp; | &nbsp; | &nbsp; |

  | start | 2 | Earliest time at location | DateTime | &nbsp; | 0\..1 | &nbsp; |
  Format : 2020-04-24T11:00:00+02:00 |

  | end | 2 | Latest time at location | DateTime | &nbsp; | 0\..1 | &nbsp; |
  Format : 2020-04-24T11:00:00+02:00 |



  &nbsp;
left_code_blocks:
  - code_block:
    title:
    language:
right_code_blocks:
  - code_block:
    title:
    language:
---
