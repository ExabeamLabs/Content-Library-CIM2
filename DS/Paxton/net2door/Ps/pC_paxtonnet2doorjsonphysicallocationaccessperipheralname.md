#### Parser Content
```Java
{
Name = "paxton-net2door-json-physical-location-access-peripheralname"
Vendor = "Paxton"
Product = "NET2DOOR"
ExtractionType = json
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
Conditions = [
""""eventtypedescription""""
""""eventid""""
""""peripheralname""""
]
Fields = [
  """exa_json_path=$.eventtime,exa_field_name=time"""
  """exa_json_path=$.peripheralname,exa_regex="*({location_city}.+?)\s*\-\s*({location_building}.+?)\s*(\(|\-|")"""
  """exa_json_path=$.peripheralname,exa_regex="*([^\-]+)\-([^\-]+)\-\s*(\s*|({location_door}.+?))(\s*\-)?\s*(IN|OUT)"""
  """exa_json_path=$.eventtypedescription,exa_field_name=action"""
  """exa_json_path=$.eventtypedescription,exa_regex="*([^\-]+\-\s*({result_reason}[^",]+))"*(,|$)"""
  """exa_json_path=$.username,exa_regex="*(?:({last_name}[^,]+),\s*({first_name}[^",]+))"*(,|$)"""
  """exa_json_path=$.cardnumber,exa_field_name=badge_id"""
  """exa_json_path=$.userid,exa_field_name=employee_id"""
  """exa_json_path=$.eventtime,exa_field_name=time"""
  """exa_regex=\(({direction}[^\)]+)\)"""
]
ParserVersion = "v1.0.0"


}
```