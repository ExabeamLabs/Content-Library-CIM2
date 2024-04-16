#### Parser Content
```Java
{
Name = unix-unix-json-user-switch-success-userstart
Vendor = "Unix"
Product = "Unix"
ExtractionType = json
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
Conditions = [
  """"type":"user_start""""
  """PAM:session_open"""
  """"result":"success""""
]
Fields = [
  """exa_json_path=$.@timestamp,exa_field_name=time""",
  """exa_json_path=$.user.name_map.uid,exa_field_name=user""",
  """exa_json_path=$.user.uid,exa_field_name=user_id""",
  """exa_json_path=$.process.pid,exa_field_name=process_id""",
  """exa_json_path=$.process,exa_regex=\{.*?"exe":"(|({process_command_line}({process_dir}[^"]+\/).*?))"""",
  """exa_json_path=$.auditd.data.acct,exa_field_name=dest_user""",
  """exa_json_path=$.host.name,exa_field_name=host"""
]
DupFields = [
  "host->dest_host", "dest_user->account"
]
ParserVersion = "v1.0.0"


}
```