#### Parser Content
```Java
{
Name = "tyco-ccure-xml-physical-location-access-objectname1"
ExtractionType = json
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
  """exa_json_path=$.messageutc,exa_field_name=time"""
  """exa_json_path=$.objectname1,exa_regex=({last_name}[^,\"]+),\s*({first_name}[^\"]+)"""
  """exa_json_path=$.objectname2,exa_field_name=location_door"""
  """exa_json_path=$.xmlmessage,exa_regex=<Card>({badge_id}.+?)</Card>"""
  """exa_json_path=$.xmlmessage,exa_regex=<StateCode>({action}.+?)</StateCode>"""
  """exa_json_path=$.xmlmessage,exa_regex=<Direction.*?>({direction}.+?)</Direction>"""
]
ParserVersion = "v1.0.0"


}
```