#### Parser Content
```Java
{
Name = microsoft-evsecurity-str-dll-load-success-4614
  ParserVersion = v1.0.0
  Vendor = Microsoft
  Product = Event Viewer - Security
  TimeFormat = "MMM dd HH:mm:ss yyyy"
  Conditions = [ """ 4614 """,""" MSWinEventLog """,""" A notification package has been loaded by the Security Account Manager""", """Microsoft-Windows-Security-Auditing"""  ]
  Fields = [
    """<\d+>\w+ \d+ \d\d:\d\d:\d\d ({host}[\w_\-\.]+)""",
    """({time}\w\w\w\s\d\d\s\d\d:\d\d:\d\d\s\d\d\d\d)""",
    """\s({event_code}4614)\s""",
    """({event_name}A notification package has been loaded by the Security Account Manager)"""
  ]


}
```