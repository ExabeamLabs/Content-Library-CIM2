#### Parser Content
```Java
{
Name = "microsoft-sysmon-json-process-create-success-processcreate"
Vendor = "Microsoft"
Product = "Sysmon"
ExtractionType = json
TimeFormat = ["yyyy-MM-dd HH:mm:ss","yyyy-MM-dd HH:mm:ss.SSS"]
Conditions = [
"""Microsoft-Windows-Sysmon""",
"""Process Create:""",
""""ParentProcessId":"""",
""""Image":"""
]
Fields = [
  """"UtcTime":"({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)""",
     """"Image":"({process_path}(({process_dir}[^"]+?)[\\\/]+)?({process_name}[^"\\\/]+))"""",
     """"TargetFilename":"({dest_process_path}(({dest_process_dir}[^"]+?)[\\\/]+)?({dest_process_name}[^"\\\/]+?(\.({file_ext}\w+))?))"""",
     """"Domain":"(NT AUTHORITY|({domain}[^"]+))""",
     """"AccountName":"(SYSTEM|({user}[\w\.\-\!\#\^\~]{1,40}\$?))""",
     """"ProcessID":({process_id}\d+)""",
     """"ProcessGuid":"({process_guid}[^"]+)""",
     """"ParentProcessGuid":"({parent_process_guid}[^"]+)""",
     """"LogonId":"({login_id}[^"]+)""",
     """"Hashes":"[^]]+MD5=({hash_md5}[^,\s]+),""",
     """"Hostname":"({host}[^"]+)""",
     """"CommandLine":"\s*({process_command_line}[^,]+?)\s*",""",
     """"ParentImage":"({parent_process_path}(({parent_process_dir}[^"]+?)[\\\/]+)?({parent_process_name}[^"\\\/]+))"""",
     """"EventID":({event_code}\d+)""",
     """ProviderGuid":"({provider_guid}[^"]+)""",
     """"Task":({task_name}\d+)""",
     """"OpcodeValue":({opcode}\d+)""",
     """"User":"(((?i)NT AUTHORITY|({domain}[^\\]+))[\\]+)?((?i)SYSTEM|LOCAL SERVICE|NETWORK SERVICE|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""",
     """"LogonGuid":"({logon_guid}[^"]+)""",
     """"Hashes":"[^]]+SHA256=({hash_sha256}[^",]+)""",
     """"ParentCommandLine":"\s*({parent_process_command_line}[^,]+?)\s*",""",
  """exa_json_path=$..UtcTime,exa_field_name=time"""
  """exa_json_path=$.EventTime,exa_field_name=time"""
  """exa_json_path=$..Image,exa_regex=({process_path}(({process_dir}[^"]+?)[\\\/]+)?({process_name}[^"\\\/]+))""""
  """exa_json_path=$.Domain,exa_regex="(NT AUTHORITY|({domain}[^"]+))"""
  """exa_json_path=$.AccountName,exa_regex=(SYSTEM|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""
  """exa_json_path=$.ProcessID,exa_field_name=process_id"""
  """exa_json_path=$..ProcessGuid,exa_field_name=process_guid"""
  """exa_json_path=$..Hashes,exa_regex="Hashes":"[^]]+MD5=({hash_md5}[^,\s]+),d"""
  """exa_json_path=$.Hostname,exa_field_name=host"""
  """exa_json_path=$.host,exa_field_name=host"""
  """exa_json_path=$..CommandLine,exa_field_name=process_command_line"""
  """exa_json_path=$..ParentImage,exa_regex=({parent_process_path}(({parent_process_dir}[^"]+?)[\\\/]+)?({parent_process_name}[^"\\\/]+))"""
  """exa_json_path=$.EventID,exa_field_name=event_code"""
  """exa_json_path=$..event_id,exa_field_name=event_code"""
  """exa_json_path=$.Task,exa_field_name=task_name"""
  """exa_json_path=$..task,exa_field_name=task_name"""
  """exa_json_path=$.OpcodeValue,exa_field_name=opcode"""
  """exa_json_path=$..opcode,exa_field_name=opcode"""
  """exa_json_path=$..User,exa_regex=(((?i)NT AUTHORITY|({domain}[^\\]+))[\\]+)?((?i)SYSTEM|LOCAL SERVICE|NETWORK SERVICE|({user}[\w\.\-\!\#\^\~]{1,40}\$?))""""
  """exa_json_path=$..LogonGuid,exa_field_name=logon_guid"""
  """exa_json_path=$..Hashes,exa_regex="Hashes":"[^]]+SHA256=({hash_sha256}[^",]+)"""
  """exa_json_path=$..ParentCommandLine,exa_field_name=parent_process_command_line"""
  """exa_json_path=$..provider_name,exa_field_name=provider_name"""
  """exa_json_path=$.winlog.user.name,exa_regex=^({user}[\w\.\-\!\#\^\~]{1,40}\$?)$"""
  """exa_json_path=$.winlog.user.domain,exa_field_name=domain"""
  """exa_json_path=$.winlog.user.identifier,exa_field_name=user_sid"""
]
DupFields = [ "host->src_host" ]
ParserVersion = "v1.0.0"


}
```