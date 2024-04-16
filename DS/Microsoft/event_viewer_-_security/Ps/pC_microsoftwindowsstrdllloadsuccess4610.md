#### Parser Content
```Java
{
Name = microsoft-windows-str-dll-load-success-4610
  ParserVersion = v1.0.0
  Vendor = Microsoft
  Product = Event Viewer - Security
  TimeFormat = "MMM dd HH:mm:ss yyyy"
  Conditions = [ """ 4610 """,""" MSWinEventLog """,""" An authentication package has been loaded by the Local Security Authority"""  ]
  Fields = [
    """<\d+>\w+ \d+ \d\d:\d\d:\d\d ({host}[\w_\-\.]+)""",
    """({time}\w\w\w\s\d\d\s\d\d:\d\d:\d\d\s\d\d\d\d)""",
    """\s({event_code}4610)\s""",
    """({event_name}An authentication package has been loaded by the Local Security Authority)""",
    """Authentication Package Name:\s*({auth_package}[^\s]+)"""
  ]


}
```