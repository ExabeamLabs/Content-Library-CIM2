#### Parser Content
```Java
{
Name = microsoft-evsecurity-str-scheduled-task-delete-4699
  Vendor = Microsoft
  Product = Event Viewer - System
  ParserVersion = "v1.0.0"
  TimeFormat = "MMM dd HH:mm:ss yyyy"
  Conditions = [""" 4699 """,""" MSWinEventLog """,""" A scheduled task was deleted""" ]
  Fields = [
   """<\d+>\w+ \d+ \d\d:\d\d:\d\d ({host}[\w_\-\.]+)""",
   """({time}\w\w\w\s\d\d\s\d\d:\d\d:\d\d\s\d\d\d\d)""",
   """\s({event_code}4699)\s""",
   """Account Name:\s*({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s*""",
   """Account Domain:\s*({domain}[^\s]+)\s*""",
   """Logon ID:\s*({login_id}[^\s]+)\s*""",
   """({event_name}A scheduled task was deleted)""",
   """Task Name:\s*\\?({task_name}.+?)\s+Task Content:"""
  ]


}
```