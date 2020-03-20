---
title: Freight offer
position_number: 1
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

  | freightOffer | Description | Type | Length | Cardinality | Constraint /
  Comment |

  | --- | --- | --- | --- | --- | --- |
  
  | offerId | Unique Id of the freight | String | &nbsp; | 1 | Readonly | 
  
  | externalId | external Id of the freight provided by the provider | String | &nbsp; | 0..1 | &nbsp; | 
  
  | paymentDue | Due date for the payment of the transport | Number | &nbsp; | 0..1 | &gt;0 | 
  
  | pickUp | Pickup information | FreightLocation | &nbsp; | 1 | &nbsp; |
  
  | delivery | Delivery information | FreightLocation | &nbsp; | 1 | &nbsp; |
  
  | freightDescritpion | &nbsp; | &nbsp; | &nbsp; | &nbsp; | &nbsp; | 
  
  | type | 2 | Goods
  type | Enum | &nbsp; | 0..1 | <p>Possible
  values:</p><ul><li>GENERAL_MERCHANDISE</li><li>SOLID_BULK</li><li>LIQUID_BULK</li><li>ABNORMAL</li><li>CONTAINER</li></ul> | &nbsp; |  | netWeight | 2 | Weight | Number | &nbsp; | 0..1 | 0-999 | &nbsp; |  | length | 2 | Length | Number | &nbsp; | 0..1 | 0-25 | &nbsp; |  | volume | 2 | Volume | Number | &nbsp; | 0..1 | 0-999 | &nbsp; |  | <p>temperatureControlled</p> | 2 | Temperature
  controlled | Boolean | &nbsp; | 0..1 | &nbsp; | <p>&nbsp;</p> |  | hazardousness.hazardous | 2 | Hazardous
  indicator | Boolean | &nbsp; | 0..1 | &nbsp; | &nbsp; |  | requiredVehicles | 2 | Required
  vehicles type | Array | &nbsp; | 0..* | <p>Possible
  values:</p><ul><li>VAN</li><li>TAUTLINER</li><li>BOX</li><li>OPEN</li><li>TRAX_WALKING_FLOOR</li><li>COIL</li><li>JUMBO</li><li>MEGATRAILER</li><li>ISOTHERMIC</li><li>REFRIGERATED</li><li>FREEZER</li><li>MULTI_TEMPERATURE</li><li>PUBLIC_WORKS_TIPPER</li><li>CEREAL_TIPPER</li><li>STEEL_TROUGH</li><li>ARMOURED_TROUGH</li><li>PALLETABLE_BULK</li><li>WALKING_FLOOR</li><li>LIQUID_TANK</li><li>PULVERULENT_TANK</li><li>FLAT</li><li>LOWLOADER</li><li>CONTAINER_20</li><li>CONTAINER_40</li><li>CONTAINER_45</li></ul> | &nbsp; |  | owner.login | 1 | Username
  of the owner of the
  offer | String | &nbsp; | 1 | &nbsp; | &nbsp; |  | addInfo.comment | 1 | Comment | String | &nbsp; | 0..1 | &nbsp; | &nbsp; | </tbody></table>


  &nbsp;


  | FreighLocation | Description | Type | Length | Cardinality | Constraint /
  Comment |

  | --- | --- | --- | --- | --- | --- |

  | address | &nbsp; | String | &nbsp; | 0\..1 | &nbsp; |

  | address.country | Country code | String | 2 | 1 | &nbsp; |

  | address.city | City | String | &nbsp; | 1 | &nbsp; |

  | address.zip | &nbsp; | String | &nbsp; | 0\..1 | &nbsp; |

  | address.coordinates | &nbsp; | &nbsp; | &nbsp; | 0\..1 | Read-Only |

  | address.coordinates.latitude | &nbsp; | Float | &nbsp; | 1 | between -90 and
  +90 |

  | address.coordinates.longitude | &nbsp; | Float | &nbsp; | 1 | between -180
  and 180 |

  | interval | &nbsp; | &nbsp; | &nbsp; | &nbsp; | &nbsp; |

  | interval.start | Earliest time at location | DateTime | &nbsp; | 0\..1 |
  Format : 2020-04-24T11:00:00+02:00 |

  | interval.end | Latest time at location | DateTime | &nbsp; | 0\..1 | Format
  : 2020-04-24T11:00:00+02:00 |


  &nbsp;
---
