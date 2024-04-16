#### Parser Content
```Java
{
Name = cisco-duo-json-app-activity-success-user
Vendor = Cisco
Product = Duo Access
ExtractionType = json
TimeFormat = ["epoch_sec","yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ"]
Conditions = [
  """"object":"""
  """"timestamp":"""
  """"event_time":"""
  """"username":"""
]
Fields = [
  """exa_json_path=$.ts,exa_field_name=time""",
  """exa_json_path=$.object,exa_field_name=object""",
  """exa_json_path=$.timestamp,exa_regex=({time}\d{10})""",
  """exa_json_path=$.username,exa_regex=({user}[\w\.\-]{1,40}\$?)""",
  """exa_json_path=$.action,exa_field_name=operation"""
]
ParserVersion = "v1.0.0"


}
```