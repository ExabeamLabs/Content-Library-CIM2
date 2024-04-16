#### Parser Content
```Java
{
Name = "tyco-ccure-json-physical-location-access-fail-doorname"
ExtractionType = json
Vendor = "Tyco"
Product = "CCURE Building Management System"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
Conditions = [
""""ntid":""""
""""personType":""""
""""doorName":""""
]
Fields = [
""""serverName":\s*\"({host}[^\"]+)""""
""""firstName":\s*\"({first_name}[^\"]+)""""
""""lastName":\s*\"({last_name}[^\"]+)""""
""""ntid":\s*\"({user}[\w\.\-]{1,40}\$?)""""
""""doorName":\s*\"({location_door}[^\"]+?)\s*""""
""""direction":\s*\"({direction}[^\"]+)""""
""""messageDateTime":\s*\"({time}\d\d\d\d\-\d\d\-\d\dT\d\d:\d\d:\d\d)"""
""""admitReject":\s*\"({result}[^\"]+)""""
  """exa_json_path=$.serverName,exa_field_name=host"""
  """exa_json_path=$.firstName,exa_field_name=first_name"""
  """exa_json_path=$.lastName,exa_field_name=last_name"""
  """exa_json_path=$.ntid,exa_field_name=user"""
  """exa_json_path=$.doorName,exa_field_name=location_door"""
  """exa_json_path=$.direction,exa_field_name=direction"""
  """exa_json_path=$.messageDateTime,exa_field_name=time"""
  """exa_json_path=$.admitReject,exa_field_name=result"""
]
DupFields = [
"location_door->location_full"
]
ParserVersion = "v1.0.0"


}
```