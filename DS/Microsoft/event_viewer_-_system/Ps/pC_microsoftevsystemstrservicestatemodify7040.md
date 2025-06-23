#### Parser Content
```Java
{
Name = microsoft-evsystem-str-service-state-modify-7040
  Vendor = Microsoft
  Product = Event Viewer - System
  ParserVersion = "v1.0.0"
  TimeFormat = "MMM dd HH:mm:ss yyyy"
  Conditions = [""" 7040 """,""" MSWinEventLog """,""" The start type of the Background Intelligent Transfer Service service was changed """ ]
  Fields = [
   """<\d+>\w+ \d+ \d\d:\d\d:\d\d ({host}[\w_\-\.]+)""",
   """({time}\w\w\w\s\d\d\s\d\d:\d\d:\d\d\s\d\d\d\d)""",
   """\s({event_code}7040)\s""",
   """The start type of the ({service_name}.+?)\sservice""",
   """({event_name}The start type of the Background Intelligent Transfer Service service was changed from auto start to demand start)"""
  ]


}
```