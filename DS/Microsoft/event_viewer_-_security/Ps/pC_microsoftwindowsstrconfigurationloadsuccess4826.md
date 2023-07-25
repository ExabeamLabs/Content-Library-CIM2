#### Parser Content
```Java
{
Name = microsoft-windows-str-configuration-load-success-4826
  ParserVersion = v1.0.0
  Vendor = Microsoft
  Product = Event Viewer - Security
  TimeFormat = "MMM dd HH:mm:ss yyyy"
  Conditions = [ """ 4826 """,""" MSWinEventLog """,""" Boot Configuration Data loaded"""  ]
  Fields = [
    """<\d+>\w+ \d+ \d\d:\d\d:\d\d ({host}[\w_\-\.]+)""",
    """({time}\w\w\w\s\d\d\s\d\d:\d\d:\d\d\s\d\d\d\d)""",
    """\s({event_code}4826)\s""",
    """({event_name}Boot Configuration Data loaded)""",
    """Account Name:\s*(-|({user}[^\s]+))\s*""",
    """Account Domain:\s*(-|({domain}[^\s]+))\s*""",
    """Logon ID:\s*({login_id}[^\s]+)\s*""",
  ]


}
```