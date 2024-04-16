#### Parser Content
```Java
{
Name = microsoft-evsystem-str-policy-apply-1500
  Vendor = Microsoft
  Product = Event Viewer - System
  ParserVersion = "v1.0.0"
  TimeFormat = "MMM dd HH:mm:ss yyyy"
  Conditions = [""" 1500 """,""" MSWinEventLog """,""" The Group Policy settings for the computer were processed successfully""" ]
  Fields = [
   """<\d+>\w+ \d+ \d\d:\d\d:\d\d ({host}[\w_\-\.]+)""",
   """({time}\w\w\w\s\d\d\s\d\d:\d\d:\d\d\s\d\d\d\d)""",
   """\s({event_code}1500)\s""",
   """({event_name}The Group Policy settings for the computer were processed successfully)"""
  ]


}
```