#### Parser Content
```Java
{
Name = microsoft-evsystem-xml-process-create-success-5861
  ParserVersion = v1.0.0
  Vendor = Microsoft
  Product = Event Viewer - System
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = [
"""<EventID>5861""",
"""Microsoft-Windows-WMI-Activity"""
  ]
  Fields = [
    """SystemTime=\'({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
    """<EventID>({event_code}[^<]+)</EventID>""",
    """<Computer>({dest_host}({host}[^<]+))</Computer>""",
    """<\d+>\w+ \d+ \d\d:\d\d:\d\d ({host}[\w_\-\.]+)""",
    """<Security UserID\\*='({user_sid}[^']+)""",
    """({process_name}WMI)""",
    """Query\s*=\s*"*({process_command_line}[^";]+)""",
    """Consumer:\s* instance of\s*({process_path}.+?)\s*\{"""
  ]


}
```