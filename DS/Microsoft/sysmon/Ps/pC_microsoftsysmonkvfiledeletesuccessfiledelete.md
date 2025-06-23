#### Parser Content
```Java
{
Name = "microsoft-sysmon-kv-file-delete-success-filedelete"
Vendor = "Microsoft"
Product = "Sysmon"
TimeFormat = "yyyy-MM-dd HH:mm:ss.SSS"
Conditions = [
  """File Delete:"""
  """IMPHASH="""
  """User:"""
]
Fields = [
  """({event_name}File Delete)"""
  """\s({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d.\d\d\d)\s"""
  """ProcessGuid:\s\{({process_guid}[^\}]+)\}"""
  """ProcessId:\s({process_id}\d+)"""
  """User:\s(NT|[^\\]+\\({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""
  """Image:\s+({process_path}({process_dir}[^"]*?[\\\/]+)?({process_name}[^\s\\\/]+))\s+\w+:"""
  """TargetFilename:\s({file_path}({file_dir}[^"]*?[\\\/]+)?({file_name}[^"\\\/]+?(\.({file_ext}\w+))?))\s+\w+:"""
  """MD5=({hash_md5}[^,]+),"""
  """SHA256=({hash_sha256}[^,]+),"""
]
ParserVersion = "v1.0.0"


}
```