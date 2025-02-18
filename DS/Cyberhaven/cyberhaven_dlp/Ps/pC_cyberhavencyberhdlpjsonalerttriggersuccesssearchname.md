#### Parser Content
```Java
{
Name = "cyberhaven-cyberhdlp-json-alert-trigger-success-searchname"
Product = "Cyberhaven DLP"
Vendor = "Cyberhaven"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
ExtractionType = json
Conditions = [ """"id":""", """search_name":""", """"file_name":""", """"source_location":""", """"source_type":""", """"destination_type":""", """"date":""", """"event_type":""", """"hostname":"""]
Fields = [
  """exa_json_path=$.id,exa_field_name=alert_id"""
  """exa_json_path=$.search_name,exa_regex=({alert_name}[^,]+), Category:\s*({category}[^"]+)"""
  """exa_json_path=$.file_name,exa_field_name=file_name"""
  """exa_json_path=$.user,exa_field_name=user"""
  """exa_json_path=$.source_type,exa_field_name=alert_type"""
  """exa_json_path=$.date,exa_regex=({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)"""
  """exa_json_path=$.source_location,exa_field_name=alert_source"""
  """exa_json_path=$.hostname,exa_field_name=host"""
]
ParserVersion = "v1.0.0"


}
```