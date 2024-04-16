#### Parser Content
```Java
{
Name = "microsoft-sysmon-json-process-create-success-createremotethread"
ExtractionType = json
Vendor = "Microsoft"
Product = "Sysmon"
TimeFormat = ["yyyy-MM-dd HH:mm:ss","yyyy-MM-dd HH:mm:ss.SSS"]
Conditions = [
"""Microsoft-Windows-Sysmon""",
"""CreateRemoteThread detected:""",
""""TargetImage":""""
]
Fields = [
  """exa_json_path=$.UtcTime,exa_field_name=time"""
  """exa_json_path=$.EventTime,exa_field_name=time"""
  """exa_json_path=$.SourceImage,exa_regex=({process_path}(({process_dir}[^"]*?)[\\\/]+)?({process_name}[^"\\\/]+))""""
  """exa_json_path=$.Domain,exa_regex=({process_path}(({process_dir}[^"]*?)[\\\/]+)?({process_name}[^"\\\/]+))"""
  """exa_json_path=$.AccountName,exa_regex=(SYSTEM|({user}[\w\.\-]{1,40}\$?))"""
  """exa_json_path=$.SourceProcessId,exa_field_name=process_id"""
  """exa_json_path=$.TargetProcessId,exa_field_name=dest_process_id"""
  """exa_json_path=$.TargetProcessGuid,exa_field_name=dest_process_id"""
  """exa_json_path=$.Hostname,exa_field_name=host"""
  """exa_json_path=$.LogonId,exa_field_name=login_id"""
  """exa_json_path=$.TargetImage,exa_regex=({dest_process}(({dest_process_dir}[^"]*?)[\\\/]+)?({dest_process_name}[^"\\\/]+))""""
  """exa_json_path=$.EventID,exa_field_name=event_code"""
  """exa_json_path=$.Category,exa_field_name=event_name"""
]
DupFields = [  "host->src_host", "dest_process->dest_process_path" ]
ParserVersion = "v1.0.0"


}
```