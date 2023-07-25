#### Parser Content
```Java
{
Name = microsoft-evsystem-str-endpoint-logout-success-7002
  Vendor = Microsoft
  Product = Event Viewer - System
  ParserVersion = "v1.0.0"
  TimeFormat = "MMM dd HH:mm:ss yyyy"
  Conditions = [""" 7002 """,""" MSWinEventLog """,""" User Logoff Notification """ ]
  Fields = [
   """<\d+>\w+ \d+ \d\d:\d\d:\d\d ({host}[\w_\-\.]+)""",
   """({time}\w\w\w\s\d\d\s\d\d:\d\d:\d\d\s\d\d\d\d)""",
   """\s({event_code}7002)\s""",
   """({event_name}User Logoff Notification for Customer Experience Improvement Program)"""
  ]


}
```