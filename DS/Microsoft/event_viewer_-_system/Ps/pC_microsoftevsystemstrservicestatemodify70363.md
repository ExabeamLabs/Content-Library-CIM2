#### Parser Content
```Java
{
Name = microsoft-evsystem-str-service-state-modify-7036-3
  ParserVersion = "v1.0.0"
  Vendor = "Microsoft"
  Product = "Event Viewer - System"
  TimeFormat = "MMM dd HH:mm:ss yyyy"
  Conditions = ["""7036""",""" MSWinEventLog""",""" service entered the running state.""" ]
  Fields = [
   """({time}\w+\s\d+\s\d+:\d+:\d+\s\d+)""",
   """\w+\s\d+\s\d+:\d+:\d+\s({host}[^\s]+)\sMSWinEventLog""",
   """\s({event_code}7036)\s""",
   """({event_name}The.+?)\s*("|$)"""
  ]


}
```