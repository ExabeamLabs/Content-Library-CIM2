#### Parser Content
```Java
{
Name = "microsoft-sysmon-kv-file-write-success-filecreate"
Vendor = "Microsoft"
Product = "Sysmon"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
  """Microsoft-Windows-Sysmon"""
  """File created:"""
]
Fields = [
  """Hostname":"({host}[^"]+?)""""
  """UtcTime:\s*({time}\d\d\d\d\-\d\d-\d\d \d\d:\d\d:\d\d)"""
  """\sComputer(?:Name)?\s*=\s*"?({host}[^\s"]+)"""
  """Message\s*=\s*"?({operation_type}[^:]+)"""
  """User\s*=\s*"(({domain}[^"]+?)[\\\/]+)?({user}[^"\\\/]+)"""
  """ProcessGuid:\s*\{({process_guid}[^\s\}]+)"""
  """ProcessId:\s*({process_id}\d+)"""
  """ParentProcessGuid:\s*\{({parent_process_guid}[^\s\}]+)"""
  """\s+Image:\s*({process_path}({process_dir}(?:(\w+:)?[^:]+)?[\\\/])?({process_name}.+?))\s+TargetFilename:"""
  """\sTargetFilename:\s*({file_path}(({file_dir}.+?)[\\\/]+)?({file_name}[^\\\/]*?(\.({file_ext}\w+))?))\s+CreationUtcTime:"""
  """EventID":({event_code}\d+),"""
  """Domain":"({domain}[^"]+?)""""
  """AccountName":"({user}[^"]+?)""""
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