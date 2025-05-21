#### Parser Content
```Java
{
Name = microsoft-evsystem-str-service-state-modify-7036-4
  Vendor = Microsoft
  Product = Event Viewer - System
  ParserVersion = "v1.0.0"
  TimeFormat = "MMM dd HH:mm:ss yyyy"
  Conditions = [""" 7036 """,""" MSWinEventLog """,""" service entered the paused state.""", """Service Control Manager""" ]
  Fields = [
   """<\d+>\w+ \d+ \d\d:\d\d:\d\d ({host}[\w_\-\.]+)""",
   """({time}\w\w\w\s\d\d\s\d\d:\d\d:\d\d\s\d\d\d\d)""",
   """\s({event_code}7036)\s""",
   """({event_name}service entered the paused state)""",
   """Information\s+\S+\s+\S+\s+(The )?({service_name}.+?)\sservice """,
  ]


}
```