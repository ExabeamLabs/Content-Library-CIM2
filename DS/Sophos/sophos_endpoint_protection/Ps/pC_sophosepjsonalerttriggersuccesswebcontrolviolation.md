#### Parser Content
```Java
{
Name = sophos-ep-json-alert-trigger-success-webcontrolviolation
ExtractionType = json
Vendor = "Sophos"
Product = "Sophos Endpoint Protection"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
Conditions = [
""""Event::Endpoint::WebControlViolation""""
""""User bypassed category block """
]
Fields = [
  """exa_json_path=$.rt,exa_field_name=time""",
  """exa_json_path=$.name,exa_regex=({alert_name}[^'"]+) to '({malware_url}[^'"]+)""",
  """exa_json_path=$.name,exa_field_name=additional_info""",
  """exa_json_path=$.type,exa_field_name=alert_type""",
  """exa_json_path=$.dhost,exa_field_name=src_host""",
  """exa_json_path=$.severity,exa_field_name=alert_severity""",
  """exa_json_path=$.suser,exa_regex=(?:n\/a|((({domain}[^\\"]+)\\+)?({full_name}({last_name}[^\\\(\)\s",]+),?\s+({first_name}[^\\\(\)",]+)))|({user}[\w\.\-\!\#\^\~]{1,40}\$?)|((({=domain}[^\\",]+)\\+)?({=user}[\w\.\-\!\#\^\~]{1,40}\$?)))$""",
  """exa_json_path=$.source,exa_regex=(?:n\/a|((({domain}[^\\"]+)\\+)?({full_name}({last_name}[^\\\(\)\s",]+),?\s+({first_name}[^\\\(\)",]+)))|({user}[\w\.\-\!\#\^\~]{1,40}\$?)|((({=domain}[^\\",]+)\\+)?({=user}[\w\.\-\!\#\^\~]{1,40}\$?)))$""",
  """exa_json_path=$.id,exa_field_name=alert_id"""
]
ParserVersion = "v1.0.0"


}
```