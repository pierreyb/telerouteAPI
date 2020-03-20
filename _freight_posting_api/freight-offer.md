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


  <table><tbody><tr><td>freightOffer</td><td>Description</td><td>Type</td><td>Cardinality</td><td>Constraint
  /
  Comment</td></tr><tr><td>&mdash;</td><td>&mdash;</td><td>&mdash;</td><td>&mdash;</td><td>&mdash;</td></tr><tr><td>offerId</td><td>Unique
  Id of the
  freight</td><td>String</td><td>1</td><td>Readonly</td></tr><tr><td>externalId</td><td>external
  Id of the freight provided by the
  provider</td><td>String</td><td>0..1</td><td>&nbsp;</td></tr><tr><td>paymentDue</td><td>Due
  date for the payment of the
  transport</td><td>Integer</td><td>0..1</td><td>&gt;0</td></tr><tr><td>pickUp</td><td>Pickup
  information</td><td>FreightLocation</td><td>1</td><td>&nbsp;</td></tr><tr><td>delivery</td><td>Delivery
  information</td><td>FreightLocation</td><td>1</td><td>&nbsp;</td></tr><tr><td>freightDescritpion</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td></tr><tr><td>freightDescritpion.type</td><td>Goods
  type</td><td>Enum</td><td>0..1</td><td><p>Possible values
  :</p><ul><li>A</li><li>B</li></ul></td></tr><tr><td>freightDescritpion.netWeight</td><td>Weight</td><td>Number</td><td>0..1</td><td>0-999</td></tr><tr><td>freightDescritpion.length</td><td>Length</td><td>Number</td><td>0..1</td><td>0-25</td></tr><tr><td>freightDescritpion.volume</td><td>Volume</td><td>Number</td><td>0..1</td><td>0-999</td></tr><tr><td>freightDescritpion.temperatureControlled</td><td>Temperature
  controlled</td><td>Boolean</td><td>0..1</td><td>&nbsp;</td></tr><tr><td>freightDescritpion.hazardousness.hazardous</td><td>Hazardous
  indicator</td><td>Boolean</td><td>0..1</td><td>&nbsp;</td></tr><tr><td>freightDescritpion.requiredVehicles</td><td>Required
  vehicles type</td><td>Array</td><td>0..*</td><td>Possible
  values</td></tr><tr><td>owner.login</td><td>Username of the owner of the
  offer</td><td>String</td><td>1</td><td>&nbsp;</td></tr><tr><td>addInfo.comment</td><td>Comment</td><td>String</td><td>0..1</td><td>&nbsp;</td></tr></tbody></table>


  &nbsp;


  | FreighLocation | Description | Type | Cardinality | Constraint / Comment |

  | --- | --- | --- | --- | --- |

  | address | &nbsp; | String | 0\..1 | &nbsp; |

  | address.country | Country code | String | 1 | supported list in reference
  data |

  | address.city | City | String | 1 | &nbsp; |

  | address.zip | &nbsp; | String | 0\..1 | &nbsp; |

  | address.coordinates | &nbsp; | &nbsp; | 0\..1 | Read-Only |

  | address.coordinates.latitude | &nbsp; | Float | 1 | between -90 and +90 |

  | address.coordinates.longitude | &nbsp; | Float | 1 | between -180 and 180 |

  | interval | &nbsp; | &nbsp; | &nbsp; | &nbsp; |

  | interval.start | Earliest time at location | DateTime | 0\..1 | Format :
  2020-04-24T11:00:00+02:00 |

  | interval.end | Latest time at location | DateTime | 0\..1 | Format :
  2020-04-24T11:00:00+02:00 |


  &nbsp;
---
