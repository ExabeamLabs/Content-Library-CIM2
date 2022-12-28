#### Parser Content
```Java
{
Name = microsoft-evsecurity-kv-endpoint-login-success-500
  Vendor = Microsoft
  Product = Event Viewer - Security
  ParserVersion = "v1.0.0"
  TimeFormat = "MM/dd/yyyy HH:mm:ss a"
  Conditions = [ """SourceName =AD FS Auditing""", """EventCode=500""" ]
  Fields = [
    """({time}\d\d\/\d\d\/\d\d\d\d \d\d:\d\d:\d\d (AM|am|PM|pm))""",
    """ComputerName =({host}[\w\-.]+)""",
    """EventCode=({event_code}\d+)""",
    """Instance ID:\s*({iid}[^\s]+)""",
    """Issued identity:.*claims/UPN\s*({user}[^@]+)@({domain}[^\s]+)""",
    """Issued identity:.*/authenticationmethod/({auth_method}[^\s]+)"""
  ]


}
```