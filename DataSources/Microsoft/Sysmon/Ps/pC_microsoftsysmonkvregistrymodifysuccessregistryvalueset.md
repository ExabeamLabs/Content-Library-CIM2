#### Parser Content
```Java
{
Name = microsoft-sysmon-kv-registry-modify-success-registryvalueset
  ParserVersion = v1.0.0
  Vendor = Microsoft
  Product = Sysmon
  TimeFormat = "yyyy-MM-dd HH:mm:ss.SSS"
  Conditions = [ """=Microsoft-Windows-Sysmon""", """Message=Registry value set:""" ]
  Fields = [
    """UtcTime:\s*({time}\d\d\d\d\-\d\d-\d\d \d\d:\d\d:\d\d\.\d\d\d)""",
    """\sComputer(?:Name)?=({host}[^\s]+)""",
    """Message=({operation_type}[^:]+)""",
    """Task=({operation}.+?)\s+(\w+=|$)""",
    """User=({user}.+?)\s+(\w+=|$)""",
    """Domain=({domain}.+?)\s+(\w+=|$)""",
    """User:\s*(?:({domain}[^\\]+)\\)?({user}.+?)\s+\w+:""",
    """ProcessGuid:\s*\{({process_guid}[^\s\}]+)""",
    """ProcessId:\s*({process_id}\d+)""",
    """\s+Image:\s*({process_path}({process_dir}(?:(\w+:)?[^:]+)?[\\\/])?({process_name}[^:]+?))\s+\w+:"""
    """\s+Image:\s*({file_path}({file_dir}(?:(\w+:)?[^:]+)?[\\\/])?({file_name}.+?))\s+\w+:"""
  ]
  DupFields = [ "host->dest_host" ]


}
```