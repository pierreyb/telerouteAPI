---
title: Vehicle offer
position_number: 1
content_markdown: >-
  Vehicle API have been upgraded to v2 (Accept-version: v2)

  {: .info}


  Vehicle offers contain the information related to available vehicle.


  *The Vehicle offer model* &nbsp;


  | VehicleOffer | Description | Type | Cardinality | Constraint / Comment |

  | --- | --- | --- | --- | --- |

  | offerId | Unique Id of the vehicle | String | 1 | Readonly |

  | externalId | external Id of the vehicle provided by the provider | String |
  0\..1 | &nbsp; |

  | departure | Departure information | VehicleLocation | 0\..1 | &nbsp; |

  | Arrival | Arrival information | VehicleLocation | 0\..1 | &nbsp; |

  | VehicleDescritpion | &nbsp; | &nbsp; | &nbsp; | &nbsp; |

  | VehicleDescritpion.type | Vehicle type | String | 1 | [reference data
  vehicle type](#reference_datavehicles-type){: target="_blank"} |

  | VehicleDescritpion.netWeight | Available weight | Number | 0\..1 | 0-999 |

  | VehicleDescritpion.length | Available length | Number | 0\..1 | 0-25 |

  | VehicleDescritpion.volume | Available volume | Number | 0\..1 | 0-999 |

  | owner.login | Username of the owner of the offer | String | 1 | &nbsp; |

  | addInfo.comment | Comment | String | 0\..1 | &nbsp; |


  &nbsp;


  | VehicleLocation | Description | Type | Cardinality | Constraint / Comment |

  | --- | --- | --- | --- | --- |

  | address | &nbsp; | String | 0\..1 | &nbsp; |

  | address.country | Country code | String | 1 | [reference country
  code](#reference_datacountry){: target="_blank"} |

  | address.city | City | String | 1 | &nbsp; |

  | address.zip | &nbsp; | String | 0\..1 | &nbsp; |

  | address.coordinates | &nbsp; | &nbsp; | 0\..1 | Read-Only |

  | address.coordinates.latitude | &nbsp; | Float | 1 | between -90 and +90 |

  | address.coordinates.longitude | &nbsp; | Float | 1 | between -180 and 180 |

  | interval | &nbsp; | &nbsp; | &nbsp; | &nbsp; |

  | interval.start | Earliest time at location | DateTime | 0\..1 | Format :
  2020-04-24T11:00:00 |

  | interval.end | Latest time at location | DateTime | 0\..1 | Format :
  2020-04-24T11:00:00 |

  | regions | &nbsp; | array | 0\..10 | [reference regions
  code](#reference_datateleroute-regions){: target="_blank"} |


  | &nbsp; | &nbsp; |

  | &nbsp; | &nbsp; |


  &nbsp;
---