#### Parser Content
```Java
{
Name = microsoft-evsystem-str-process-close-5186
  Vendor = Microsoft
  Product = Event Viewer - System
  ParserVersion = "v1.0.0"
  TimeFormat = "MMM dd HH:mm:ss yyyy"
  Conditions = [  """ 5186 """, """ shutdown due to inactivity.""",""" MSWinEventLog """ ]
  Fields = [
     """<\d+>\w+ \d+ \d\d:\d\d:\d\d ({host}[\w_\-\.]+)""",
     """({time}\w\w\w\s\d\d\s\d\d:\d\d:\d\d\s\d\d\d\d)""",
     """({event_code}5186)""",
     """process id of '({process_id}\d+)"""
  ]


}
```