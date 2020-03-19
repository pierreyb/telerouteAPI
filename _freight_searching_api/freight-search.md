---
title: Freight search
position_number: 1
type:
description:
parameters:
  - name:
    content:
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


  Freight search data model


  <table><thead><tr><th><p>freightSearches</p></th><th><p>L</p></th><th><p>Description</p></th><th><p>Type</p></th><th><p>Length</p></th><th><p>Cardinality</p></th><th><p>Constraint</p></th><th><p>Comment</p></th></tr></thead><tbody><tr><td>searchId</td><td>1</td><td>Unique
  Id of the
  search</td><td>String</td><td>&nbsp;</td><td>1</td><td>Readonly</td><td>&nbsp;</td></tr><tr><td>state</td><td>1</td><td>Status
  of the search</td><td>Enum</td><td>&nbsp;</td><td>1</td><td><p>Possible
  values:</p><ul><li>ACTIVE</li><li>UNACTIVE</li></ul></td><td>&nbsp;</td></tr><tr><td>departure</td><td>1</td><td>Departure
  criteria of the
  search</td><td>FreightSearchLocation</td><td>&nbsp;</td><td>0..1</td><td>&nbsp;</td><td><p>if
  not present arrival is mandatory &nbsp;<a
  href="https://issues.wkts.eu/browse/FX-15187">FX-15187</a>&nbsp;- [FX-API] -
  freightSearch - address model - radius should be part of the
  address&nbsp;<strong>CLOSED</strong></p></td></tr><tr><td>arrival</td><td>1</td><td>Arrival
  criteria of the
  search</td><td>FreightSearchLocation</td><td>&nbsp;</td><td>0..1</td><td>&nbsp;</td><td><p>if
  not present departure is mandatory &nbsp;<a
  href="https://issues.wkts.eu/browse/FX-15187">FX-15187</a>&nbsp;- [FX-API] -
  freightSearch - address model - radius should be part of the
  address&nbsp;<strong>CLOSED</strong></p></td></tr><tr><td>loadingInterval</td><td>1</td><td>Loading
  criteria of the
  search</td><td>&nbsp;</td><td>&nbsp;</td><td>1</td><td>&nbsp;</td><td><p><a
  href="https://issues.wkts.eu/browse/FX-15129">FX-15129</a>&nbsp;- [FX-API] -
  freightSearch - loading interval should be only start and end
  date&nbsp;<strong>CLOSED</strong></p></td></tr><tr><td>loadingTime</td><td>2</td><td>fix
  type of
  interval&nbsp;</td><td>Enum</td><td>&nbsp;</td><td>0..1</td><td><p>Possible
  value</p><ul><li>NO_DATE</li><li>AS_OF</li><li>UNTIL</li><li>BETWEEN</li><li>ON</li><li>D0
  # Departure date is today</li><li>D1 # Departure date is tomorrow</li><li>D0D1
  # Departure date is today or tomorrow</li><li>D0D1D2 # Departure date is
  today, tommorrow or day after tomorrow</li><li>D1D2 # Departure date is
  tomorrow or day after
  tomorrow</li></ul></td><td><p>&nbsp;</p></td></tr><tr><td>start</td><td>2</td><td>Start
  date criteria for the
  search</td><td>Date</td><td>&nbsp;</td><td>0..1</td><td>&nbsp;</td><td><p>format
  : 2019-04-05 (&nbsp;<a
  href="https://issues.wkts.eu/browse/FX-15128">FX-15128</a>&nbsp;- [FX-API] -
  freightSearch - date and time should be without
  timezone&nbsp;<strong>CLOSED</strong>&nbsp;)</p></td></tr><tr><td>end</td><td>2</td><td>End
  date criteria for the
  search&nbsp;</td><td>Date</td><td>&nbsp;</td><td>0..1</td><td>&nbsp;</td><td><p>format
  : 2019-04-05 (&nbsp;<a
  href="https://issues.wkts.eu/browse/FX-15128">FX-15128</a>&nbsp;- [FX-API] -
  freightSearch - date and time should be without
  timezone&nbsp;<strong>CLOSED</strong>&nbsp;)</p></td></tr><tr><td>loadingDescritpion</td><td>1</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td></tr><tr><td>goods</td><td>2</td><td>Goods
  type</td><td>Enum</td><td>&nbsp;</td><td>0..1</td><td><p>Possible
  values:</p><ul><li>GENERAL_MERCHANDISE</li><li>SOLID_BULK</li><li>LIQUID_BULK</li><li>ABNORMAL</li><li>CONTAINER</li></ul></td><td>&nbsp;</td></tr><tr><td>weight</td><td>2</td><td>Weight</td><td>Integer</td><td>&nbsp;</td><td>0..1</td><td>0-999</td><td>&nbsp;</td></tr><tr><td>length</td><td>2</td><td>Length</td><td>Integer</td><td>&nbsp;</td><td>0..1</td><td>0-25</td><td>&nbsp;</td></tr><tr><td>volume</td><td>2</td><td>Volume</td><td>Integer</td><td>&nbsp;</td><td>0..1</td><td>0-999</td><td>&nbsp;</td></tr><tr><td><p>temperatureControlled</p></td><td>2</td><td>Only
  search for temperature controlled
  freight</td><td>Boolean</td><td>&nbsp;</td><td>0..1</td><td>&nbsp;</td><td><p>if
  goods = "TEMPERATURE_CONTROLLED" then TRUE</p><p>else
  FALSE</p></td></tr><tr><td>hazardous</td><td>2</td><td>Only search for
  hazardous
  freight</td><td>Boolean</td><td>&nbsp;</td><td>0..1</td><td>&nbsp;</td><td>&nbsp;</td></tr><tr><td>Vehicles</td><td>2</td><td>Required
  vehicles type</td><td>String</td><td>&nbsp;</td><td>0..*</td><td><p>Possible
  values:</p><ul><li>VAN</li><li>TAUTLINER</li><li>BOX</li><li>OPEN</li><li>TRAX_WALKING_FLOOR</li><li>COIL</li><li>JUMBO</li><li>MEGATRAILER</li><li>ISOTHERMIC</li><li>REFRIGERATED</li><li>FREEZER</li><li>MULTI_TEMPERATURE</li><li>PUBLIC_WORKS_TIPPER</li><li>CEREAL_TIPPER</li><li>STEEL_TROUGH</li><li>ARMOURED_TROUGH</li><li>PALLETABLE_BULK</li><li>WALKING_FLOOR</li><li>LIQUID_TANK</li><li>PULVERULENT_TANK</li><li>FLAT</li><li>LOWLOADER</li><li>CONTAINER_20</li><li>CONTAINER_40</li><li>CONTAINER_45</li></ul></td><td>&nbsp;</td></tr><tr><td>extendedSearch</td><td>1</td><td>Indicator
  that the search is an extended
  area</td><td>Boolean</td><td>&nbsp;</td><td>0..1</td><td>&nbsp;</td><td>Can
  only be true for a city to city search</td></tr></tbody></table>


  | FreightSearchLocation | L | Description | Type | Length | Cardinality |
  Constraint | Comment |

  | --- | --- | --- | --- | --- | --- | --- | --- |

  | address | 1 | City | String | &nbsp; | 0\..1 | &nbsp; | &nbsp; |

  | country | 2 | Country code | String | 2 | 1 | &nbsp; | &nbsp; |

  | city | 2 | City | String | &nbsp; | 1 | &nbsp; | &nbsp; |

  | postalCode | 2 | &nbsp; | String | &nbsp; | 0\..1 | &nbsp; | &nbsp; |

  | radius | 2 | &nbsp; | Integer | &nbsp; | 1 | values: 10, 30, 50, 100 |
  &nbsp; |

  | coordinates | 2 | &nbsp; | &nbsp; | &nbsp; | 0\..1 | Read-Only | &nbsp; |

  | latitude | 3 | &nbsp; | Float | &nbsp; | 1 | between -90 and +90 | &nbsp; |

  | longitude | 3 | &nbsp; | Float | &nbsp; | 1 | between -180 and 180 | &nbsp;
  |

  | regions | 1 | List of regions | Enum | &nbsp; | 0\..10 | &nbsp; |
  [Teleroutes
  regions.xls](https://portal.wkts.eu/download/attachments/71672562/Teleroute%20Regions.xlsx)
  |


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
