#### Parser Content
```Java
{
Name = netiq-netiqim-json-app-login-success-usersession
  ParserVersion = v1.0.0
  Vendor = NetIQ
  Product = Micro Focus NetIQ Identity Manager
  TimeFormat = "epoch"
  Conditions = [ """"NetIQ Access Manager"""", """User session""", """ siem: {""" ]
  Fields = [
    """\Wdt"*:"*({time}\d{13})""",
    """\w+ \d+ \d\d:\d\d:\d\d ({host}[A-Fa-f:\d.]+)""",
    """\Wsun"*:"*({user}[^\s,"]+)""",
    """\Wcn=({user}[^\s,]+)""",
    """Client IP Address:\s*\[({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """\WReason:\s*\[({failure_reason}[^\]]+?)\s*\]""",
    """((U|u)ser\s*Agent)\\"*:\\"*({user_agent}[^"]+?)\\*"""",
    """({app}NetIQ)""",
 ]


}
```