#### Parser Content
```Java
{
Name = "tanium-ep-json-alert-trigger-success-accountenumeration"
ExtractionType = json
Product = "Tanium Threat Response"
Vendor = "Tanium"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
Conditions = [
"""Intel Id"""
"""Intel Type"""
"""Intel Name"""
"""Intel Labels"""
]
Fields = [
  """exa_json_path=$.['Alert Id'],exa_field_name=alert_id"""
  """exa_json_path=$.Timestamp,exa_field_name=time"""
  """exa_json_path=$.['Computer Name'],exa_field_name=host"""
  """exa_json_path=$.['Computer IP'],exa_field_name=dest_ip"""
  """exa_json_path=$.['Intel Type'],exa_field_name=alert_type"""
  """exa_json_path=$.['Intel Name'],exa_field_name=alert_name"""
  """exa_json_path=$.['Intel Name'],exa_field_name=alert_name"""
  """exa_json_path=$.['Match Details'].match..file.fullpath,exa_regex=({process_path}({process_dir}[^"]+)\\+({process_name}[^"]+))"""
  """exa_json_path=$.['Match Details'].match.properties.file.md5,exa_field_name=hash_md5"""
  """exa_json_path=$.['Match Details'].match.properties,exa_regex=[^\]]+?args\\?"+:"*\\*"+({process_command_line}[^,\]]+?)\\?\s*","""
  """exa_regex="user"+:"+(?:(?:NT AUTHORITY|({domain}[^\\"]+))\\+)?(?:SYSTEM|LOCAL SERVICE|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"+\}\,"+source"+:"""
  """exa_json_path=$.['Match Details'].match.properties.user,exa_regex=([^\\]+\\+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""
  """exa_json_path=$.['Match Details'].match.properties.parent.file.fullpath,exa_regex=(({parent_process_path}({parent_process_dir}[^"]+)\\+({parent_process_name}[^"]+)))"""
]
DupFields = [
"process_path->path"
]
ParserVersion = "v1.0.0"


}
```