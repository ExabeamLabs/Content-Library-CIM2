#### Parser Content
```Java
{
Name = microsoft-evsystem-str-service-state-modify-7036-1
  Vendor = Microsoft
  Product = Event Viewer - System
  ParserVersion = "v1.0.0"
  TimeFormat = ["MMM dd HH:mm:ss yyyy", "yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ"]
  Conditions = ["""7036""",""" MSWinEventLog""",""" service entered the stopped state.""", """Service Control Manager""" ]
  Fields = [
   """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d{6}[\+\-]\d{1,2}:\d{1,2})(\s({host}[\w\-.]+)\s)?""",
   """({time}\w+\s\d+\s\d+:\d+:\d+\s\d+)""",
   """\w+\s\d+\s\d+:\d+:\d+\s({host}[^\s]+)\sMSWinEventLog""",
   """\s({event_code}7036)\s""",
   """({event_name}The.+?)\s*("|$)"""
  ]


}
```