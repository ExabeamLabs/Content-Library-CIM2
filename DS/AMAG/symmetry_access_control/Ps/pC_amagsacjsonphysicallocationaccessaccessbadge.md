#### Parser Content
```Java
{
Name = "amag-sac-json-physical-location-access-accessbadge"
Vendor = "AMAG"
Product = "Symmetry Access Control"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
ExtractionType = json
Conditions = [
  """"access_badge""""
  """"txnconditionname":""""
  """"cardnumber":"""
]
Fields = [
  """exa_json_path=$.datetimeoftxn,exa_field_name=time""",
  """exa_json_path=$.txnconditionname,exa_field_name=action"""
  """exa_json_path=$.wherename,exa_field_name=location_door""",
  """exa_json_path=$.firstname,exa_field_name=first_name"""
  """exa_json_path=$.lastname,exa_field_name=last_name"""
  """exa_json_path=$.cardnumber,exa_field_name=badge_id""",
  """exa_json_path=$.db_name,exa_field_name=direction"""
  """exa_json_path=$.db_ip,exa_regex=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
]
ParserVersion = "v1.0.0"


}
```