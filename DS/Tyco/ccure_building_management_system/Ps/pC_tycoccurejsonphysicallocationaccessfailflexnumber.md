#### Parser Content
```Java
{
Name = "tyco-ccure-json-physical-location-access-fail-flexnumber"
Vendor = "Tyco"
Product = "CCURE Building Management System"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
Conditions = [ """"messagetype":"Card""", """"statecode":"""", """"primaryobjectname":""" ]
Fields = [
  """"messageutc":"({time}[^"]+)""",
  """"statecode":"({event_name}[^"]+)""",
  """"messagetype":"({result}[^"]+)""",
  """"primaryobjectname":"*(null|({last_name}[^",]+?)\s*,\s*({first_name}[^",]+?))\s*"""",
  """"secondaryobjectname":"+(null|({location_door}[^"]+))""",
]
ParserVersion = "v1.0.0"


}
```