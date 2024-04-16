#### Parser Content
```Java
{
Name = "timelox-t-json-physical-location-access-doorgroupname"
ExtractionType = json
Vendor = "TimeLox"
Product = "TimeLox"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
Conditions = [
  """"eventtime":""""
  """"doorgroupname":""""
  """"issued by":"""
]
Fields = [
  """exa_json_path=$.doorgroupname,exa_field_name=door_group_name"""
  """exa_json_path=$.eventtime,exa_field_name=time"""
  """exa_json_path=$.userid,exa_field_name=user_id"""
  """exa_json_path=$.event,exa_field_name=action"""
  """exa_json_path=$.['issued by'],exa_field_name=user"""
  """exa_json_path=$.door,exa_field_name=location_door"""
  """exa_json_path=$.blockinggroupname,exa_field_name=blocking_group_name"""
  """exa_json_path=$.['user group'],exa_field_name=user_group_name"""
  """exa_json_path=$.['registration no.'],exa_field_name=registration_no"""
  """exa_regex="@version":"({version}[^"]+)"""
]
ParserVersion = "v1.0.0"


}
```