#### Parser Content
```Java
{
Name = microsoft-sysmon-kv-process-close-success-processterminated
  Vendor = Microsoft
  Product = Sysmon
  ParserVersion = v1.0.0
  TimeFormat = [ "yyyy-MM-dd HH:mm:ss", "yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ" ]
  Conditions = [ """Microsoft-Windows-Sysmon""", """Process terminated:""" ]
  Fields = [
    """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d{6}[\+\-]\d{1,2}:\d{1,2})(\s({host}[\w\-.]+)\s)?""",
    """Hostname":"({host}[^"]+?)"""",
    """UtcTime:\s*({time}\d\d\d\d\-\d\d-\d\d \d\d:\d\d:\d\d)""",
    """\sComputer(?:Name)?\s*=\s*"?({host}[^\s"]+)""",
    """Message\s*=\s*"?({operation_type}[^:]+)""",
    """User\s*=\s*"(({domain}[^"]+?)[\\\/]+)?({user}[\w\.\-]{1,40}\$?)""",
    """ProcessGuid:\s*\{({process_guid}[^\s\}]+)""",
    """ProcessId:\s*({process_id}\d+)""",
    """\s+Image:\s*({process_path}({process_dir}(?:(\w+:)?[^:]+)?[\\\/])?({process_name}.+?))\s*";""",
    """"Image":"({process_path}(({process_dir}[^"]*?)[\\\/]+)?({process_name}[^"\\\/]+))"""",
    """EventID":({event_code}\d+),""",
  ]
  DupFields = [ "host->dest_host" ]


}
```