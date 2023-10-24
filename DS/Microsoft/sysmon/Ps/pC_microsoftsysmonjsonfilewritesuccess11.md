#### Parser Content
```Java
{
Name = "microsoft-sysmon-json-file-write-success-11"
Vendor = "Microsoft"
Product = "Sysmon"
TimeFormat = "yyyy-MM-dd HH:mm:ss.SSS"
Conditions = [
  """Microsoft-Windows-Sysmon"""
  """File created"""
  """"AccountName":""""
  """"EventID":11"""
]
Fields = [
  """"UtcTime":"({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d\.\d\d\d)"""
  """"Image":"({process_path}(({process_dir}[^"]*?)[\\\/]+)?({process_name}[^"\\\/]+))""""
  """"TargetFilename":"({file_path}(({file_dir}[^"]*?)[\\\/]+)?({file_name}[^"\\\/]+?(\.({file_ext}\w+))?))""""
  """"Domain":"((?i)NT AUTHORITY|({domain}[^"]+))"""
  """"AccountName":"((?i)SYSTEM|({user}[\w\.\-]{1,40}\$?))"""
  """"ProcessID":({process_id}\d+)"""
  """"Hostname":"({host}[^"]+)"""
  """Category":"({event_name}[^"]+)"""
  """"CreationUtcTime":"({creation_utc_time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d.\d\d\d)"""
  """EventID":({event_code}\d+)"""
]
ParserVersion = "v1.0.0"


}
```