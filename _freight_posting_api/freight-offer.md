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


  &nbsp;


  \| freightOffer \| Description \| Type \| Length \| Cardinality \| Constraint
  / Comment \| \| — \| — \| — \| — \| — \| — \| \| offerId \| Unique Id of the
  freight \| String \| &nbsp; \| 1 \| Readonly \| \| externalId \| external Id
  of the freight provided by the provider \| String \| &nbsp; \| 0..1 \| &nbsp;
  \| \| paymentDue \| Due date for the payment of the transport \| Integer \|
  &nbsp; \| 0..1 \| &gt;0 \| \| pickUp \| Pickup information \| FreightLocation
  \| &nbsp; \| 1 \| &nbsp; \| \| delivery \| Delivery information \|
  FreightLocation \| &nbsp; \| 1 \| &nbsp; \| \| freightDescritpion \| &nbsp; \|
  &nbsp; \| &nbsp; \| &nbsp; \| &nbsp; \| \| freightDescritpion.type \| Goods
  type \| Enum \| &nbsp; \| 0..1 \| Possible values \| \|
  freightDescritpion.netWeight \| Weight \| Number \| &nbsp; \| 0..1 \| 0-999 \|
  \| freightDescritpion.length \| Length \| Number \| &nbsp; \| 0..1 \| 0-25
  \|<br>\| freightDescritpion.volume \| Volume \| Number \| &nbsp; \| 0..1 \|
  0-999 \| \| freightDescritpion.temperatureControlled \| Temperature controlled
  \| Boolean \| &nbsp; \| 0..1 \| &nbsp; \| \|
  freightDescritpion.hazardousness.hazardous \| Hazardous indicator \| Boolean
  \| &nbsp; \| 0..1 \| &nbsp; \| \| freightDescritpion.requiredVehicles \|
  Required vehicles type \| Array \| &nbsp; \| 0..\* \| Possible values \| \|
  owner.login \| Username of the owner of the offer \| String \| &nbsp; \| 1 \|
  &nbsp; \|<br>\| addInfo.comment \| Comment \| String \| &nbsp; \| 0..1 \|
  &nbsp; \|


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
