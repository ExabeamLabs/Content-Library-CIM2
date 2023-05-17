#### Parser Content
```Java
{
Name = windows-evsystem-xml-endpoint-notification-12
  ParserVersion = v1.0.0
  Vendor = Microsoft
  Product = Event Viewer - System
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSSZ"
  Conditions = [ """<EventID>12<""", """<Provider>Microsoft-Windows-Wininit""", """was started as a protected process with level:""" ]
  Fields = [
    """<TimeCreated SystemTime\\*='({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z)""",
    """<Computer>({dest_host}({host}[\w\-.]+))""",
    """<\d+>\w+ \d+ \d\d:\d\d:\d\d ({host}[\w_\-\.]+)""",
    """<EventID>({event_code}12)<""",
    """<Message>({event_name}[^<]+)<""",
    """<EventRecordID>({event_id}\d+)<""",
    """<Execution ProcessID\\*='({process_id}\d+)'""",
    """ThreadID\\*='({thread_id}\d+)'""",
    """<Security UserID\\*='({user_sid}[^']+)'""",
    """<Provider>({provider_name}[^<]+)<""",
    """<Message>({process_name}\S+)\swas started as a protected process with level"""
  ]


}
```