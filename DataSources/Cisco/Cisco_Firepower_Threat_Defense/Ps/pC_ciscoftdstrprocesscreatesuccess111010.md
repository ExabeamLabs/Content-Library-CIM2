#### Parser Content
```Java
{
Name = cisco-ftd-str-process-create-success-111010
  ParserVersion = v1.0.0
  Vendor = Cisco
  Product = Cisco Firepower Threat Defense
  TimeFormat = "MMM dd yyyy HH:mm:ss"
  Conditions = [ """-111010""", """%FTD-""" ]
  Fields = [
    """({time}\w+ \d+ \d\d\d\d \d\d:\d\d:\d\d)\s+({host}[\w\-.]+)\s*:\s*%FTD""",
    """%FTD\-({priority}\d+)\-({event_code}\d+)""",
    """User\s+'({user}[^']+)'""",
    """({event_name}executed)\s+'({process_command_line}[^']+?)\s*'""",
    """from IP (0.0.0.0|({src_ip}[A-Fa-f:\d.]+))"""
  ]


}
```