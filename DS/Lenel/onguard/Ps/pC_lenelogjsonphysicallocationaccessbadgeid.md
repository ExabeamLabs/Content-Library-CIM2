#### Parser Content
```Java
{
Name = "lenel-og-json-physical-location-access-badgeid"
ExtractionType = json
Vendor = "Lenel"
Product = "OnGuard"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
Conditions = [
  """"cardholder_first_name":"""
  """"badge_id":"""
]
Fields = [
  """exa_json_path=$.timestamp,exa_field_name=time""",
  """exa_json_path=$.badge_id,exa_field_name=badge_id""",
  """exa_json_path=$.cardholder_first_name,exa_field_name=first_name""",
  """exa_json_path=$.cardholder_last_name,exa_field_name=last_name""",
  """exa_json_path=$.device_name,exa_field_name=location_door""",
  """exa_json_path=$.description,exa_field_name=action""",
]
ParserVersion = "v1.0.0"


}
```