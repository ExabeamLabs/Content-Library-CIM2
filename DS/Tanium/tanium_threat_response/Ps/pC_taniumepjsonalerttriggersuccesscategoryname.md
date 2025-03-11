#### Parser Content
```Java
{
Name = "tanium-ep-json-alert-trigger-success-categoryname"
ExtractionType = json
Product = "Tanium Threat Response"
Vendor = "Tanium"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
Conditions = [
"""Intel Id"""
"""Intel Type"""
"""Intel Name"""
"""Intel Labels"""
""""detection_id"""
""""category_name""""
]
Fields = [
  """exa_json_path=$.['Alert Id'],exa_field_name=alert_id"""
  """exa_json_path=$.Timestamp,exa_field_name=time"""
  """exa_json_path=$.['Computer Name'],exa_field_name=host"""
  """exa_json_path=$.['Computer IP'],exa_field_name=dest_ip"""
  """exa_json_path=$.['Intel Type'],exa_field_name=alert_type"""
  """exa_json_path=$.['Intel Name'],exa_field_name=alert_name"""
  """exa_json_path=$.['Match Details'].finding.whats..additional_fields.threat_name,exa_field_name=alert_name"""
  """exa_json_path=$.['Match Details'].finding.whats..additional_fields.category_name,exa_field_name=alert_type"""
  """exa_json_path=$.['Match Details'].finding.whats..additional_fields.severity_name,exa_field_name=alert_severity"""
  """exa_json_path=$.['Match Details'].match..file.fullpath,exa_regex=({process_path}({process_dir}[^"]+)\\+({process_name}[^"]+))"""
  """exa_regex="user"+:\{.+?"user"+:.+?"name"+:"+({user}[\w\.\-\!\#\^\~]{1,40}\$?)""""
  """exa_json_path=$.['Match Details']..detection_user,exa_regex=((({domain}[^\\"]+)\\+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""
  """exa_regex="detection_user":"((({domain}[^\\"]+)\\+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""
  """exa_json_path=$.['Match Details']..system_info.platform,exa_field_name=os"""
]
DupFields = [
"process_path->path"
]
ParserVersion = "v1.0.0"


}
```