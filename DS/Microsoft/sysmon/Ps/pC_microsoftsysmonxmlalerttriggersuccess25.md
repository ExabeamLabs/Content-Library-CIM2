#### Parser Content
```Java
{
Name = microsoft-sysmon-xml-alert-trigger-success-25
  ParserVersion = v1.0.0
  Vendor = Microsoft
  Product = Sysmon
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSSZ"
  Conditions = [ """<Provider Name""", """<EventID>25</EventID>""", """Microsoft-Windows-Sysmon""" ]
  Fields = [
    """<TimeCreated SystemTime\\*=('|")({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d.\d{1,9}Z)""",
    """<Computer>({dest_host}({host}[\w\-.]+))""",
    """<\d+>\w+ \d+ \d\d:\d\d:\d\d ({host}[\w_\-\.]+)""",
    """<EventID>({event_code}25)""",
    """ProcessID\\*='({process_id}\d+)'""",
    """ThreadID\\*='({thread_id}\d+)'""",
    """<Security UserID\\*='({user_sid}[^']+)'""",
    """Guid\\*='\{({process_guid}[^'}]+)""",
    """({alert_name}Process Tampering)""",
    """<Data Name ='Image'>({process_path}({process_dir}[^<>"]*?[\\\/]+)?({process_name}[^"<>\\\/]*))<\/Data>"""
    """<Level>({run_level}[^<]+)<"""
  ]


}
```