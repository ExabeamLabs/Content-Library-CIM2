#### Parser Content
```Java
{
Name = microsoft-evsecurity-str-share-create-success-5142
  Vendor = Microsoft
  Product = Event Viewer - System
  ParserVersion = "v1.0.0"
  TimeFormat = "MMM dd HH:mm:ss yyyy"
  Conditions = [""" 5142 """,""" MSWinEventLog """,""" A network share object was added""" ]
  Fields = [
   """<\d+>\w+ \d+ \d\d:\d\d:\d\d ({host}[\w_\-\.]+)""",
   """({time}\w\w\w\s\d\d\s\d\d:\d\d:\d\d\s\d\d\d\d)""",
   """\s({event_code}5142)\s""",
   """({event_name}A network share object was added)""",
   """Account Name:\s*({user}[\w\.\-]{1,40}\$?)\s*""",
   """Account Domain:\s*({domain}[^\s]+)\s*""",
   """Share Name:\s*\\\\\*\\({share_name}.+?)\s+Share Path:\s+(\s+|({share_path}.+?))\s""",
   """({result}\S+)\sAudit"""
  ]


}
```