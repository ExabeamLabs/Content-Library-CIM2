#### Parser Content
```Java
{
Name = "microsoft-sysmon-kv-file-write-success-filecreate"
Vendor = "Microsoft"
Product = "Sysmon"
TimeFormat = [ "yyyy-MM-dd HH:mm:ss", "yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ" ]
Conditions = [
  """Microsoft-Windows-Sysmon"""
  """File created:"""
]
Fields = [
  """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d{6}[\+\-]\d{1,2}:\d{1,2})(\s({host}[\w\-.]+)\s)?""",
  """Hostname":"({host}[\w\-.]+?)""""
  """UtcTime:\s*({time}\d\d\d\d\-\d\d-\d\d \d\d:\d\d:\d\d)"""
  """\sComputer(?:Name)?\s*=\s*"?({host}[\w\-.]+)"""
  """Message\s*=\s*"?({operation_type}[^:]+)"""
  """User\s*=\s*"(({domain}[^"]+?)[\\\/]+)?({user}[\w\.\-]{1,40}\$?)"""
  """ProcessGuid:\s*\{({process_guid}[^\s\}]+)"""
  """ProcessId:\s*({process_id}\d+)"""
  """ParentProcessGuid:\s*\{({parent_process_guid}[^\s\}]+)"""
  """\s+Image:\s*({process_path}({process_dir}(?:(\w+:)?[^:]+)?[\\\/])?({process_name}.+?))\s+TargetFilename:"""
  """\sTargetFilename:\s*({file_path}(({file_dir}.+?)[\\\/]+)?({file_name}[^\\\/]*?(\.({file_ext}\w+))?))\s+CreationUtcTime:"""
  """EventID":({event_code}\d+),"""
  """Domain":"({domain}[^"]+?)""""
  """AccountName":"({user}[\w\.\-]{1,40}\$?)""""
  """"Image":"({process_path}(({process_dir}[^"]*?)[\\\/]+)?({process_name}[^"\\\/]+))""""
  """"TargetFilename":"({file_path}(({file_dir}[^"]+?)[\\\/]+)?({file_name}[^"\\\/]+?(\.({file_ext}\w+))?))""""
]
DupFields = [
  "host->dest_host"
  "process_path->path"
]
ParserVersion = "v1.0.0"


}
```