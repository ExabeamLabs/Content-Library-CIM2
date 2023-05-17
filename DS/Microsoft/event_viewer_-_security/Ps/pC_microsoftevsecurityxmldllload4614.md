#### Parser Content
```Java
{
Name = microsoft-evsecurity-xml-dll-load-4614
  Vendor = Microsoft
  Product = Event Viewer - Security
  ParserVersion = v1.0.0
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSSZ"
  Conditions = [ """>4614<""", """Microsoft-Windows-Security-Auditing""", """<Data Name""","""'NotificationPackageName'>""" ]
  Fields = [
    """({event_name}Microsoft-Windows-Security-Auditing)""",
    """<TimeCreated SystemTime\\*='({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z)""",
    """<Computer>({src_host}[^<>]+)<\/Computer>""",
    """<\d+>\w+ \d+ \d\d:\d\d:\d\d ({host}[\w_\-\.]+)""",
    """({event_code}4614)""",
    """ProcessID\\*='({process_id}\d+)'""",
    """ThreadID\\*='({thread_id}\d+)'""",
    """<Keyword>({result}[^<]+)<""",
    """<Data Name\\*='NotificationPackageName'>({object}[^<]+)<""",
    """({event_name}A notification package has been loaded by the Security Account Manager)"""
  ]


}
```