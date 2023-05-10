#### Parser Content
```Java
{
Name = microsoft-evsecurity-xml-endpoint-notification-5031
  Vendor = Microsoft
  ParserVersion = "v1.0.0"
  Product = Event Viewer - System
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = [ """<EventID>5031<""", """Windows Firewall blocked an application from accepting incoming connections on the network""" ]
  Fields = [
    """<EventID>({event_code}\d+)""",
    """({event_name}Windows Firewall blocked an application from accepting incoming connections on the network.)""",
    """<TimeCreated SystemTime='({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
    """<Computer>({host}[^<]+)""",
    """<Execution ProcessID='({process_id}\d+)' ThreadID='({thread_id}\d+)'""",
    """<Data Name ='Application'>({process_path}({process_dir}(?:[^<]+)?[\\\/])?({process_name}[^\\\/]+?))<\/Data>"""
  ]


}
```