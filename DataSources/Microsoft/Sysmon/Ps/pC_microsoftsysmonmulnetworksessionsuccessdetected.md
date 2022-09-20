#### Parser Content
```Java
{
Name = microsoft-sysmon-mul-network-session-success-detected
  ParserVersion = v1.0.0
  Vendor = Microsoft
  Product = Sysmon
  TimeFormat = "yyyy-MM-dd HH:mm:ss.SSS"
  Conditions = [
"""Microsoft-Windows-Sysmon""",
"""Network connection detected:"""
  ]
  Fields = [
    """UtcTime:\s*({time}\d\d\d\d\-\d\d-\d\d \d\d:\d\d:\d\d\.\d\d\d)""",
    """Hostname":"({host}[^"]+?)"""",
    """\sComputer(?:Name)?\s*=\s*"?({host}[^\s"]+)""",
    """Computer>({host}[^<]+)<\/Computer""",
    """Message\s*=\s*"?({operation_type}[^:]+)""",
    """Task="*}({operation}[^=]+?)"*}\s+(\w+=|$)""",
    """User=({user}[^=]+?)\s+(\w+=|$)""",
    """Domain=({domain}[^=]+?)\s+(\w+=|$)""",
    """User:\s*(?:({domain}[^\\]+)\\+)?({user}[^:]+?)\s+\w+:""",
    """Protocol:\s*({protocol}[^\s]+)""",
    """ProcessGuid:\s*\{({process_guid}[^\s\}]+)""",
    """ProcessId:\s*({process_id}\d+)""",
    """\s+Image:\s*({process_path}({process_dir}(?:(\w+:)?[^:]+)?[\\\/])?({process_name}[^:]+?))\s+\w+:""",
    """SourceIp:\s*({src_ip}[a-fA-F0-9.:]+)""",
    """SourceHostname:\s*({src_host}[^\s]+?)\s*(Source|$)""",
    """SourcePort:\s*({src_port}\d+)""",
    """DestinationIp:\s*({dest_ip}[a-fA-F0-9.:]+)""",
    """DestinationHostname:\s*(-|({dest_host}[^\s]+?))\s*(Destination|$)""",
    """DestinationPort:\s*({dest_port}\d+)""",
    """\sInitiated:\s*({initiated}[^\s]+)""",
    """EventID":({event_code}\d+),""",
    """"Image":"({process_path}(({process_dir}[^"]*00}?)[\\\/]+)?({process_name}[^"\\\/]+))""""
  ]


}
```