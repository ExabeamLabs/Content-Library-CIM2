#### Parser Content
```Java
{
Name = "tyco-ccure-xml-physical-location-access-objectname1"
Vendor = "Tyco"
Product = "CCURE Building Management System"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
Conditions = [
  """objectname2"""
  """objectname1"""
  """<Card>"""
  """<StateCode>"""
]
Fields = [
  """"messageutc\":\"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z)\""""
  """"objectname1\":\"({last_name}[^,\"]+),\s*({first_name}[^\"]+)\""""
  """"objectname2\":\"({location_door}[^\"]+)\""""
  """<Card>({badge_id}.+?)</Card>"""
  """<StateCode>({action}.+?)</StateCode>"""
  """<Direction.*?>({direction}.+?)</Direction>"""
]
ParserVersion = "v1.0.0"


}
```