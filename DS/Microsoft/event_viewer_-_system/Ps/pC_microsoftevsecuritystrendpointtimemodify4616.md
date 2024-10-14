#### Parser Content
```Java
{
Name = microsoft-evsecurity-str-endpoint-time-modify-4616
  Vendor = Microsoft
  Product = Event Viewer - System
  ParserVersion = "v1.0.0"
  TimeFormat = "MMM dd HH:mm:ss yyyy"
  Conditions = [""" 4616 """,""" MSWinEventLog """,""" The system time was changed""" ]
  Fields = [
   """<\d+>\w+ \d+ \d\d:\d\d:\d\d ({host}[\w_\-\.]+)""",
   """({time}\w\w\w\s\d\d\s\d\d:\d\d:\d\d\s\d\d\d\d)""",
   """\s({event_code}4616)\s""",
   """({event_name}The system time was changed)""",
   """Account Name:\s*({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s*""",
   """Account Domain:\s*(-|({domain}[^:]+?))\s*Logon ID:\s*({login_id}\S+)""",
   """Process ID:\s*({process_id}\S+)\s*Name:\s*({process_path}({process_dir}[^\s]+)\\+({process_name}[^\s]+))"""
  ]


}
```