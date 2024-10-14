#### Parser Content
```Java
{
Name = "microsoft-sysmon-json-file-write-success-11"
ExtractionType = json
Vendor = "Microsoft"
Product = "Sysmon"
TimeFormat = "yyyy-MM-dd HH:mm:ss.SSS"
Conditions = [
  """"Channel":"Microsoft-Windows-Sysmon"""
  """File created"""
  """"AccountName":""""
  """"EventID":11"""
]
Fields = [
  """"UtcTime":"({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d\.\d\d\d)"""
  """"Image":"({process_path}(({process_dir}[^"]*?)[\\\/]+)?({process_name}[^"\\\/]+))""""
  """"TargetFilename":"({file_path}(({file_dir}[^"]*?)[\\\/]+)?({file_name}[^"\\\/]+?(\.({file_ext}\w+))?))""""
  """"Domain":"((?i)NT AUTHORITY|({domain}[^"]+))"""
  """"AccountName":"((?i)SYSTEM|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""
  """"ProcessID":({process_id}\d+)"""
  """"Hostname":"({host}[^"]+)"""
  """Category":"({event_name}[^"]+)"""
  """"CreationUtcTime":"({creation_utc_time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d.\d\d\d)"""
  """EventID":({event_code}\d+)"""
  """exa_json_path=$.UtcTime,exa_field_name=time"""
  """exa_regex="Image":"({process_path}(({process_dir}[^"]*?)[\\\/]+)?({process_name}[^"\\\/]+))""""
  """exa_regex="TargetFilename":"({file_path}(({file_dir}[^"]*?)[\\\/]+)?({file_name}[^"\\\/]+?(\.({file_ext}\w+))?))""""
  """exa_json_path=$.Domain,exa_field_name=domain"""
  """exa_json_path=$.AccountName,exa_field_name=user"""
  """exa_json_path=$.ProcessID,exa_field_name=process_id"""
  """exa_json_path=$.Hostname,exa_field_name=host"""
  """exa_json_path=$.CreationUtcTime,exa_field_name=creation_utc_time"""
  """exa_json_path=$.EventID,exa_field_name=event_code"""
]
ParserVersion = "v1.0.0"


}
```