#### Parser Content
```Java
{
Name = microsoft-evsystem-str-endpoint-notification-16
  Vendor = Microsoft
  Product = Event Viewer - System
  ParserVersion = "v1.0.0"
  TimeFormat = "MMM dd HH:mm:ss yyyy"
  Conditions = [""" 16 """,""" MSWinEventLog """,""" The access history in hive """ ]
  Fields = [
   """<\d+>\w+ \d+ \d\d:\d\d:\d\d ({host}[\w_\-\.]+)""",
   """({time}\w\w\w\s\d\d\s\d\d:\d\d:\d\d\s\d\d\d\d)""",
   """\s({event_code}16)\s""",
   """({event_name}The access history in hive)"""
  ]


}
```