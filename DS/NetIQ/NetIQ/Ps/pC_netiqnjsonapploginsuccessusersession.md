#### Parser Content
```Java
{
Name = netiq-n-json-app-login-success-usersession
  ParserVersion = v1.0.0
  Vendor = NetIQ
  Product = NetIQ
  TimeFormat = "epoch"
  Conditions = [ """"NetIQ Access Manager"""", """User session""", """ siem: {""" ]
  Fields = [
    """\Wdt"*:"*({time}\d+)""",
    """\w+ \d+ \d\d:\d\d:\d\d ({host}[A-Fa-f:\d.]+)""",
    """\Wsun"*:"*({user}[^\s,"]+)""",
    """\Wcn=({user}[^\s,]+)""",
    """Client IP Address:\s*\[({src_ip}[A-Fa-f:\d.]+)""",
    """\WReason:\s*\[({failure_reason}[^\]]+?)\s*\]""",
    """((U|u)ser\s*Agent)\\"*:\\"*({user_agent}[^"]+?)\\*"""",
    """({app}NetIQ)""",
 ]


}
```