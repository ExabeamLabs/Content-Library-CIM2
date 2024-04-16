#### Parser Content
```Java
{
Name = microsoft-evapp-str-policy-apply-fail-4098
  Vendor = Microsoft
  Product = Event Viewer - Application
  ParserVersion = "v1.0.0"
  TimeFormat = "MMM dd HH:mm:ss yyyy"
  Conditions = [ """ 4098 """, """ Group Policy Object did not apply """,""" MSWinEventLog """ ]
  Fields = [
    """({event_name}Group Policy Object did not apply)""",
    """<\d+>\w+ \d+ \d\d:\d\d:\d\d ({host}[\w_\-\.]+)""",
    """({time}\w\w\w\s\d\d\s\d\d:\d\d:\d\d\s\d\d\d\d)""",
    """({event_code}4098)""",
    """error code '({error_code}[^\s]+)\s"""
  ]


}
```