#### Parser Content
```Java
{
Name = microsoft-evapp-str-app-activity-success-5973
  Vendor = Microsoft
  Product = Event Viewer - Application
  ParserVersion = "v1.0.0"
  TimeFormat = "MMM dd HH:mm:ss yyyy"
  Conditions = [ """ 5973 """, """ activated by the Built-in Administrator""",""" MSWinEventLog """ ]
  Fields = [
    """<\d+>\w+ \d+ \d\d:\d\d:\d\d ({host}[\w_\-\.]+)""",
    """({time}\w\w\w\s\d\d\s\d\d:\d\d:\d\d\s\d\d\d\d)""",
    """({event_code}5973)""",
  ]


}
```