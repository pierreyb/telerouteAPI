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


  <table><thead><tr><th><p>freightOffer</p></th><th><p>L</p></th><th><p>Description</p></th><th><p>Type</p></th><th><p>Length</p></th><th><p>Cardinality</p></th><th><p>Constraint</p></th><th><p>Comment</p></th></tr></thead><thead><tr><th><p>freightOffer</p></th><th><p>L</p></th><th><p>Description</p></th><th><p>Type</p></th><th><p>Length</p></th><th><p>Cardinality</p></th><th><p>Constraint</p></th><th><p>Comment</p></th></tr></thead><tbody><tr><td>offerId</td><td>1</td><td>Unique
  Id of the
  freight</td><td>String</td><td>&nbsp;</td><td>1</td><td>Readonly</td><td>&nbsp;</td></tr><tr><td>externalId</td><td>1</td><td>external
  Id of the freight provided by the
  provider</td><td>String</td><td>&nbsp;</td><td>0..1</td><td>&nbsp;</td><td>&nbsp;</td></tr><tr><td>paymentDue</td><td>1</td><td>Due
  date for the payment of the
  transport</td><td>Number</td><td>&nbsp;</td><td>0..1</td><td>&gt;0</td><td>&nbsp;</td></tr><tr><td>pickUp</td><td>1</td><td>Pickup
  information</td><td>FreightLocation</td><td>&nbsp;</td><td>1</td><td>&nbsp;</td><td><p>&nbsp;</p></td></tr><tr><td>delivery</td><td>1</td><td>Delivery
  information</td><td>FreightLocation</td><td>&nbsp;</td><td>1</td><td>&nbsp;</td><td><p>&nbsp;</p></td></tr><tr><td>freightDescritpion</td><td>1</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td></tr><tr><td>type</td><td>2</td><td>Goods
  type</td><td>Enum</td><td>&nbsp;</td><td>0..1</td><td><p>Possible
  values:</p><ul><li>GENERAL_MERCHANDISE</li><li>SOLID_BULK</li><li>LIQUID_BULK</li><li>ABNORMAL</li><li>CONTAINER</li></ul></td><td>&nbsp;</td></tr><tr><td>netWeight</td><td>2</td><td>Weight</td><td>Number</td><td>&nbsp;</td><td>0..1</td><td>0-999</td><td>&nbsp;</td></tr><tr><td>length</td><td>2</td><td>Length</td><td>Number</td><td>&nbsp;</td><td>0..1</td><td>0-25</td><td>&nbsp;</td></tr><tr><td>volume</td><td>2</td><td>Volume</td><td>Number</td><td>&nbsp;</td><td>0..1</td><td>0-999</td><td>&nbsp;</td></tr><tr><td><p>temperatureControlled</p></td><td>2</td><td>Temperature
  controlled</td><td>Boolean</td><td>&nbsp;</td><td>0..1</td><td>&nbsp;</td><td><p>&nbsp;</p></td></tr><tr><td>hazardousness.hazardous</td><td>2</td><td>Hazardous
  indicator</td><td>Boolean</td><td>&nbsp;</td><td>0..1</td><td>&nbsp;</td><td>&nbsp;</td></tr><tr><td>requiredVehicles</td><td>2</td><td>Required
  vehicles type</td><td>Array</td><td>&nbsp;</td><td>0..*</td><td><p>Possible
  values:</p><ul><li>VAN</li><li>TAUTLINER</li><li>BOX</li><li>OPEN</li><li>TRAX_WALKING_FLOOR</li><li>COIL</li><li>JUMBO</li><li>MEGATRAILER</li><li>ISOTHERMIC</li><li>REFRIGERATED</li><li>FREEZER</li><li>MULTI_TEMPERATURE</li><li>PUBLIC_WORKS_TIPPER</li><li>CEREAL_TIPPER</li><li>STEEL_TROUGH</li><li>ARMOURED_TROUGH</li><li>PALLETABLE_BULK</li><li>WALKING_FLOOR</li><li>LIQUID_TANK</li><li>PULVERULENT_TANK</li><li>FLAT</li><li>LOWLOADER</li><li>CONTAINER_20</li><li>CONTAINER_40</li><li>CONTAINER_45</li></ul></td><td>&nbsp;</td></tr><tr><td>owner.login</td><td>1</td><td>Username
  of the owner of the
  offer</td><td>String</td><td>&nbsp;</td><td>1</td><td>&nbsp;</td><td>&nbsp;</td></tr><tr><td>addInfo.comment</td><td>1</td><td>Comment</td><td>String</td><td>&nbsp;</td><td>0..1</td><td>&nbsp;</td><td>&nbsp;</td></tr></tbody></table>


  &nbsp;


  | FreighLocation | Description | Type | Length | Cardinality | Constraint / Comment |

  | --- | --- | --- | --- | --- | --- | 

  | address |  | String | &nbsp; | 0\..1 | &nbsp; | 

  | address.country | Country code | String | 2 | 1 | &nbsp; | 

  | address.city | City | String | &nbsp; | 1 | &nbsp; | 

  | address.zip | &nbsp; | String | &nbsp; | 0\..1 | &nbsp; | 

  | address.coordinates | &nbsp; | &nbsp; | &nbsp; | 0\..1 | Read-Only | 

  | address.coordinates.latitude | &nbsp; | Float | &nbsp; | 1 | between -90 and +90 | 

  | address.coordinates.longitude | &nbsp; | Float | &nbsp; | 1 | between -180 and 180 | 

  | interval | &nbsp; | &nbsp; | &nbsp; | &nbsp; | &nbsp; | 

  | interval.start | Earliest time at location | DateTime | &nbsp; | 0\..1 | 
  Format : 2020-04-24T11:00:00+02:00 |

  | interval.end | Latest time at location | DateTime | &nbsp; | 0\..1 | 
  Format : 2020-04-24T11:00:00+02:00 |


  &nbsp;
---
