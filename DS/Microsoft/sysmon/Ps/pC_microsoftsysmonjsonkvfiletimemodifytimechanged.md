#### Parser Content
```Java
{
Name = microsoft-sysmon-json-kv-file-time-modify-timechanged
  ParserVersion = v1.0.0
  Vendor = Microsoft
  Product = Sysmon
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """File creation time changed: """, """ UtcTime: """ ]
  Fields = [
    """UtcTime:\s*({time}\d\d\d\d\-\d\d-\d\d \d\d:\d\d:\d\d)""",
    """Message\s*=\s*"?({operation_type}[^:]+)""",
    """User\s*=\s*"(({domain}[^"]+?)[\\\/]+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)""",
    """ProcessGuid:\s*\{({process_guid}[^\s\}]+)""",
    """ProcessId:\s*({process_id}\d+)""",
    """\s+Image:\s*({process_path}({process_dir}(?:(\w+:)?[^:]+)?[\\\/])?({process_name}[^=]+?))\s*";"""
    """\sTargetFilename:\s*({file_path}(({file_dir}[^=]+?)[\\\/]+)?({file_name}[^\\\/]*?(\.({file_ext}\w+))?))\s+CreationUtcTime:""",
  ]


}
```