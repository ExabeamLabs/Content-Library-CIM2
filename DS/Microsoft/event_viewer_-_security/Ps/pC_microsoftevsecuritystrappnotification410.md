#### Parser Content
```Java
{
Name = microsoft-evsecurity-str-app-notification-410
  Vendor = Microsoft
  Product = Event Viewer - Security
  ParserVersion = "v1.0.0"
  TimeFormat = "MMM dd HH:mm:ss yyyy"
  Conditions = [  """ 410 """, """ Following request context headers present """,""" MSWinEventLog """, """AD FS Auditing""" ]
  Fields = [
    """<\d+>\w+ \d+ \d\d:\d\d:\d\d ({host}[\w_\-\.]+)""",
    """({time}\w\w\w\s\d\d\s\d\d:\d\d:\d\d\s\d\d\d\d)""",
    """({event_code}410)""",
  ]


}
```