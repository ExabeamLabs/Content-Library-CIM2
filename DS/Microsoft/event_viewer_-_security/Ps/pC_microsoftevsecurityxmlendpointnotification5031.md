#### Parser Content
```Java
{
Name = microsoft-evsecurity-xml-endpoint-notification-5031
  Vendor = Microsoft
  ParserVersion = "v1.0.0"
  Product = Event Viewer - Security
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = [ """<EventID>5031<""", """Microsoft-Windows-Security-Auditing""","""<Channel>Security</Channel>""" ]
  Fields = [
    """<EventID>({event_code}\d+)""",
    """({event_name}Windows Firewall blocked an application from accepting incoming connections on the network.)""",
    """<TimeCreated SystemTime\\*=('|")({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
    """<Computer>({host}[^<]+)""",
    """<\d+>\w+ \d+ \d\d:\d\d:\d\d ({host}[\w_\-\.]+)""",
    """<Execution ProcessID\\*='({process_id}\d+)' ThreadID\\*='({thread_id}\d+)'""",
    """<Data Name\\*='Application'>({process_path}({process_dir}(?:[^<]+)?[\\\/])?({process_name}[^\\\/]+?))<\/Data>"""
    """<Level>({run_level}[^<]+)<"""
  ]


}
```