#### Parser Content
```Java
{
Name = microsoft-evsystem-xml-process-create-success-5861
  ParserVersion = v1.0.0
  Vendor = Microsoft
  Product = Microsoft WMI Log
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = [
"""<EventID>5861""",
"""Microsoft-Windows-WMI-Activity"""
"""<Channel>Microsoft-Windows-WMI-Activity/Operational</Channel>"""
  ]
  Fields = [
    """SystemTime=('|")({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
    """<EventID>({event_code}[^<]+)</EventID>""",
    """<Computer>({dest_host}({host}[\w\-.]+))</Computer>""",
    """<\d+>\w+ \d+ \d\d:\d\d:\d\d ({host}[\w_\-\.]+)""",
    """<Security UserID\\*=('|")({user_sid}[^'"]+)""",
    """({process_name}WMI)""",
    """Query\s*=\s*"*({process_command_line}[^";]+)""",
    """Consumer:\s* instance of\s*({additional_info}.+?)\s*\{""",
    """<Level>({run_level}[^<]+)<"""
  ]


}
```