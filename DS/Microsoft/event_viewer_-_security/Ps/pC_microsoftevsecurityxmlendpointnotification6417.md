#### Parser Content
```Java
{
Name = microsoft-evsecurity-xml-endpoint-notification-6417
  ParserVersion = v1.0.0
  Vendor = Microsoft
  Product = Event Viewer - Security
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = [ """<EventID>6417<""", """Microsoft-Windows-Security-Auditing""" ]
  Fields = [
    """<EventID>({event_code}\d+)""",
    """({event_name}The FIPS mode crypto selftests succeeded.)""",
    """<TimeCreated SystemTime\\*=('|")({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
    """<Computer>({host}[^<]+)""",
    """<\d+>\w+ \d+ \d\d:\d\d:\d\d ({host}[\w_\-\.]+)""",
    """<Execution ProcessID\\*='({process_id}\d+)' ThreadID\\*='({thread_id}\d+)'""",
    """<Data Name[^<>]+?ProcessName[^<>]+?>(-|({process_path}({process_dir}[^<>]*?[\\\/]+)?({process_name}[^<>\\\/]+)))</Data>"""
    """<Level>({run_level}[^<]+)<"""
  ]


}
```