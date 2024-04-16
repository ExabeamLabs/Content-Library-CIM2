#### Parser Content
```Java
{
Name = microsoft-evsystem-str-endpoint-login-success-7001
  Vendor = Microsoft
  Product = Event Viewer - System
  ParserVersion = "v1.0.0"
  TimeFormat = "MMM dd HH:mm:ss yyyy"
  Conditions = [""" 7001 """,""" MSWinEventLog """,""" User Logon Notification for Customer Experience Improvement Program""" ]
  Fields = [
   """<\d+>\w+ \d+ \d\d:\d\d:\d\d ({host}[\w_\-\.]+)""",
   """({time}\w\w\w\s\d\d\s\d\d:\d\d:\d\d\s\d\d\d\d)""",
   """\s({event_code}7001)\s""",
   """({event_name}User Logon Notification for Customer Experience Improvement Program)"""
  ]


}
```