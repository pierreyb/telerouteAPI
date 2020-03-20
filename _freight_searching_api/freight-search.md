---
title: Freight search
position_number: 1
content_markdown: >-
  A freight search will query the freight offers list to retrieve corresponding
  records. The characteristics of the search for freight offer are:


  * An origin and a destination (both are optional but not mutually optional –
  ie at least one of origin or destination is mandatory). The possible choice
  for theses value are either&nbsp;
    * A city (search is then performed based on a circle around this city)
    * A list of countries, regions or sub-region
  * A search period. ie a date range (example : Today, Today until Tomorrow,
  until a date, starting from a date, … )

  * Freight characteristics provides the type of goods to be searched.

  * Truck characteristics allow a restriction on the type of trucks to be used
  for the transportation.


  #### Freight search data model


  | freightSearches  | Description | Type | Cardinality | Constraint / Comment |
  
  | --- | --- | --- | --- | --- |
  
  | searchId | Unique Id of the search | String | 1 | Readonly |
  
  | state | 1 | Status
  of the search | Enum | &nbsp; | 1 | <p>Possible
  values:</p><ul><li>ACTIVE</li><li>UNACTIVE</li></ul> | &nbsp; | departure | 1 | Departure
  criteria of the
  search | FreightSearchLocation | &nbsp; | 0..1 | &nbsp; | <p>if
  not present arrival is mandatory &nbsp;<a
  href="https://issues.wkts.eu/browse/FX-15187">FX-15187</a>&nbsp;- [FX-API] -
  freightSearch - address model - radius should be part of the
  address&nbsp;<strong>CLOSED</strong></p> | arrival | 1 | Arrival
  criteria of the
  search | FreightSearchLocation | &nbsp; | 0..1 | &nbsp; | <p>if
  not present departure is mandatory &nbsp;<a
  href="https://issues.wkts.eu/browse/FX-15187">FX-15187</a>&nbsp;- [FX-API] -
  freightSearch - address model - radius should be part of the
  address&nbsp;<strong>CLOSED</strong></p> | loadingInterval | 1 | Loading
  criteria of the
  search | &nbsp; | &nbsp; | 1 | &nbsp; | <p><a
  href="https://issues.wkts.eu/browse/FX-15129">FX-15129</a>&nbsp;- [FX-API] -
  freightSearch - loading interval should be only start and end
  date&nbsp;<strong>CLOSED</strong></p> | loadingTime | 2 | fix
  type of
  interval&nbsp; | Enum | &nbsp; | 0..1 | <p>Possible
  value</p><ul><li>NO_DATE</li><li>AS_OF</li><li>UNTIL</li><li>BETWEEN</li><li>ON</li><li>D0
  # Departure date is today</li><li>D1 # Departure date is tomorrow</li><li>D0D1
  # Departure date is today or tomorrow</li><li>D0D1D2 # Departure date is
  today, tommorrow or day after tomorrow</li><li>D1D2 # Departure date is
  tomorrow or day after
  tomorrow</li></ul> | <p>&nbsp;</p> | start | 2 | Start
  date criteria for the
  search | Date | &nbsp; | 0..1 | &nbsp; | <p>format
  : 2019-04-05 (&nbsp;<a
  href="https://issues.wkts.eu/browse/FX-15128">FX-15128</a>&nbsp;- [FX-API] -
  freightSearch - date and time should be without
  timezone&nbsp;<strong>CLOSED</strong>&nbsp;)</p> | end | 2 | End
  date criteria for the
  search&nbsp; | Date | &nbsp; | 0..1 | &nbsp; | <p>format
  : 2019-04-05 (&nbsp;<a
  href="https://issues.wkts.eu/browse/FX-15128">FX-15128</a>&nbsp;- [FX-API] -
  freightSearch - date and time should be without
  timezone&nbsp;<strong>CLOSED</strong>&nbsp;)</p> | loadingDescritpion | 1 | &nbsp; | &nbsp; | &nbsp; | &nbsp; | &nbsp; | &nbsp; | goods | 2 | Goods
  type | Enum | &nbsp; | 0..1 | <p>Possible
  values:</p><ul><li>GENERAL_MERCHANDISE</li><li>SOLID_BULK</li><li>LIQUID_BULK</li><li>ABNORMAL</li><li>CONTAINER</li></ul> | &nbsp; | weight | 2 | Weight | Integer | &nbsp; | 0..1 | 0-999 | &nbsp; | length | 2 | Length | Integer | &nbsp; | 0..1 | 0-25 | &nbsp; | volume | 2 | Volume | Integer | &nbsp; | 0..1 | 0-999 | &nbsp; | <p>temperatureControlled</p> | 2 | Only
  search for temperature controlled
  freight | Boolean | &nbsp; | 0..1 | &nbsp; | <p>if
  goods = "TEMPERATURE_CONTROLLED" then TRUE</p><p>else
  FALSE</p> | hazardous | 2 | Only search for
  hazardous
  freight | Boolean | &nbsp; | 0..1 | &nbsp; | &nbsp; | Vehicles | 2 | Required
  vehicles type | String | &nbsp; | 0..* | <p>Possible
  values:</p><ul><li>VAN</li><li>TAUTLINER</li><li>BOX</li><li>OPEN</li><li>TRAX_WALKING_FLOOR</li><li>COIL</li><li>JUMBO</li><li>MEGATRAILER</li><li>ISOTHERMIC</li><li>REFRIGERATED</li><li>FREEZER</li><li>MULTI_TEMPERATURE</li><li>PUBLIC_WORKS_TIPPER</li><li>CEREAL_TIPPER</li><li>STEEL_TROUGH</li><li>ARMOURED_TROUGH</li><li>PALLETABLE_BULK</li><li>WALKING_FLOOR</li><li>LIQUID_TANK</li><li>PULVERULENT_TANK</li><li>FLAT</li><li>LOWLOADER</li><li>CONTAINER_20</li><li>CONTAINER_40</li><li>CONTAINER_45</li></ul> | &nbsp; | extendedSearch | 1 | Indicator
  that the search is an extended
  area | Boolean | &nbsp; | 0..1 | &nbsp; | Can
  only be true for a city to city search</td></tr></tbody></table>

   &nbsp;

  | FreightSearchLocation | Description | Type | Cardinality |
  Constraint / Comment |

  | --- | --- | --- | --- | --- |

  | address | &nbsp; | String | 0\..1 | &nbsp; |

  | address.country | Country code | String | 1 | see supported list in reference data |

  | address.city | City | String | 1 | &nbsp; |

  | address.postalCode | &nbsp; | String | 0\..1 | &nbsp; |

  | address.radius | &nbsp; | Integer | 1 | values: 10, 30, 50, 100 |

  | address.coordinates | &nbsp; | &nbsp; | 0\..1 | Read-Only |

  | address.coordinates.latitude | &nbsp; | Float | 1 | between -90 and +90 |

  | address.coordinates.longitude | &nbsp; | Float | 1 | between -180 and 180 |

  | regions | List of regions | Enum | 0\..10 | see supported list in reference data |


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
