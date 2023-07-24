#### Parser Content
```Java
{
Name = microsoft-evsecurity-str-service-create-success-4622
  Vendor = Microsoft
  Product = Event Viewer - System
  ParserVersion = "v1.0.0"
  TimeFormat = "MMM dd HH:mm:ss yyyy"
  Conditions = [""" 4622 """,""" MSWinEventLog """,""" A security package has been loaded by the Local Security Authority""" ]
  Fields = [
   """<\d+>\w+ \d+ \d\d:\d\d:\d\d ({host}[\w_\-\.]+)""",
   """({time}\w\w\w\s\d\d\s\d\d:\d\d:\d\d\s\d\d\d\d)""",
   """\s({event_code}4622)\s""",
   """({event_name}A security package has been loaded by the Local Security Authority)""",
   """Security Package Name:\s*({service_name}\S+)"""
  ]


}
```