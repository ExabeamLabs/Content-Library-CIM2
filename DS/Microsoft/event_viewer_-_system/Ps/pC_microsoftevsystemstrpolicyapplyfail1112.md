#### Parser Content
```Java
{
Name = microsoft-evsystem-str-policy-apply-fail-1112
  ParserVersion = v1.0.0
  Vendor = Microsoft
  Product = Event Viewer - System
  TimeFormat = "MMM dd HH:mm:ss yyyy"
  Conditions = [ """ 1112 """,""" MSWinEventLog """,""" The Group Policy Client Side Extension """, """Microsoft-Windows-GroupPolicy"""  ]
  Fields = [
    """<\d+>\w+ \d+ \d\d:\d\d:\d\d ({host}[\w_\-\.]+)""",
    """({time}\w\w\w\s\d\d\s\d\d:\d\d:\d\d\s\d\d\d\d)""",
    """\s({event_code}1112)\s"""
  ]


}
```