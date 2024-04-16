#### Parser Content
```Java
{
Name = "tyco-ccure-json-physical-location-access-fail-flexnumber"
ExtractionType = json
Vendor = "Tyco"
Product = "CCURE Building Management System"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
Conditions = [ """"messagetype":"Card""", """"statecode":"""", """"primaryobjectname":""" ]
Fields = [
  """exa_json_path=$.messageutc,exa_field_name=time"""
  """exa_json_path=$.statecode,exa_field_name=event_name"""
  """exa_json_path=$.messagetype,exa_field_name=result"""
  """exa_json_path=$.primaryobjectname,exa_regex=(null|({last_name}[^",]+?)\s*,\s*({first_name}[^",]+))"""
  """exa_json_path=$.secondaryobjectname,exa_field_name=location_door"""
]
ParserVersion = "v1.0.0"


}
```