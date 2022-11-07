#### Parser Content
```Java
{
Name = microsoft-evsecurity-kv-endpoint-login-fail-411
  Vendor = Microsoft
  Product = Event Viewer - Security
  ParserVersion = "v1.0.0"
  TimeFormat = "MM/dd/yyyy HH:mm:ss a"
  Conditions = [ """SourceName =AD FS""", """EventCode=411""", """Keywords=Audit Failure""" ]
  Fields = [
    """({time}\d\d\/\d\d\/\d\d\d\d \d\d:\d\d:\d\d (AM|am|PM|pm))""",
    """ComputerName =({host}[\w\-.]+)""",
    """EventCode=({event_code}\d+)""",
    """Client IP:\s*({src_ip}[A-Fa-f:\d.]+)""",
    """Error message:\s*({user}.+?)-The user name""",
    """Error message:\s*({failure_reason}.+?)\s+Exception details:"""
  ]


}
```