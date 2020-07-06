---
title: Freight search
position_number: 1
content_markdown: >-
  A freight search will query the freight offers list to retrieve corresponding
  records. The characteristics of the search for freight offer are:


  * An origin and a destination (both are optional but not mutually optional –
  ie at least one of origin or destination is mandatory). The possible choice
  for these value are either&nbsp;
    * A city (search is then performed based on a circle around this city)
    * A list of countries, regions or sub-region
  * A search period. ie a date range (example : Today, Today until Tomorrow,
  until a date, starting from a date, … )

  * Freight characteristics provide the type of goods to be searched.

  * Truck characteristics allow a restriction on the type of trucks to be used
  for the transportation.


  #### Freight search data model


  | freightSearches | Description | Type | Cardinality | Constraint / Comment |

  | --- | --- | --- | --- | --- |

  | searchId | Unique Id of the search | String | 1 | Readonly |

  | state | Status of the search | Enum | 1 | Possible values: ACTIVE or
  UNACTIVE |

  | departure | Departure criteria of the search | FreightSearchLocation | 1 |
  &nbsp; |

  | arrival | Arrival criteria of the search | FreightSearchLocation | 1 |
  &nbsp; |

  | loadingInterval | Loading criteria of the search | &nbsp; | &nbsp; | 1 |

  | loadingInterval.loadingTime | fix type of interval | Enum | 0\..1 | Possible
  value : NO\_DATE, AS\_OF, UNTIL, BETWEEN, ON, D0, D1, D0D1, D0D1D2, D1D2 |

  | loadingInterval.start | Start date criteria for the search | Date | 0\..1 |
  format : 2019-04-05 |

  | loadingInterval.end | End date criteria for the search | Date | 0\..1 |
  format : 2019-04-05 |

  | loadingDescritpion | &nbsp; | &nbsp; | &nbsp; | &nbsp; |

  | loadingDescritpion.goods | Goods type | Enum | 0\..1 | [reference data goods
  type](#reference_datagoods-type){: target="_blank"} |

  | loadingDescritpion.weight | Weight | Integer | 0\..1 | 0-999 |

  | loadingDescritpion.length | Length | Integer | 0\..1 | 0-25 |

  | loadingDescritpion.volume | Volume | Integer | 0\..1 | 0-999 |

  | loadingDescritpion.temperatureControlled | Only search for temperature
  controlled freight | Boolean | 0\..1 | &nbsp; |

  | loadingDescritpion.hazardous | Only search for hazardous freight | Boolean |
  0\..1 | &nbsp; |

  | Vehicles | Required vehicles type | String | 0\..\* | [reference data
  vehicle](#reference_datavehicles-type){: target="_blank"} |


  &nbsp;


  | FreightSearchLocation | Description | Type | Cardinality | Constraint /
  Comment |

  | --- | --- | --- | --- | --- |

  | address | &nbsp; | String | 0\..1 | &nbsp; |

  | address.country | Country code | String | 1 | [reference country code](#reference_datacountry){: target="_blank"} |

  | address.city | City | String | 1 | &nbsp; |

  | address.postalCode | &nbsp; | String | 0\..1 | &nbsp; |

  | address.radius | &nbsp; | Integer | 1 | values: 10, 30, 50, 100 |

  | address.coordinates | &nbsp; | &nbsp; | 0\..1 | Read-Only |

  | address.coordinates.latitude | &nbsp; | Float | 1 | between -90 and +90 |

  | address.coordinates.longitude | &nbsp; | Float | 1 | between -180 and 180 |

  | regions | List of regions | Enum | 0\..10 | [reference regions code](#reference_datateleroute-regions){: target="_blank"} |


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
