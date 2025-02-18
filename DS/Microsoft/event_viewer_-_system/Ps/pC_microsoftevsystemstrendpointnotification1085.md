#### Parser Content
```Java
{
Name = microsoft-evsystem-str-endpoint-notification-1085
  ParserVersion = v1.0.0
  Vendor = Microsoft
  Product = Event Viewer - System
  TimeFormat = "MMM dd HH:mm:ss yyyy"
  Conditions = [ """ 1085 """,""" MSWinEventLog """,""" failed to apply """, """Microsoft-Windows-GroupPolicy"""  ]
  Fields = [
    """<\d+>\w+ \d+ \d\d:\d\d:\d\d ({host}[\w_\-\.]+)""",
    """({time}\w\w\w\s\d\d\s\d\d:\d\d:\d\d\s\d\d\d\d)""",
    """\s({event_code}1085)\s"""
  ]


}
```