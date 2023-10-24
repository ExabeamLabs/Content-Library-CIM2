#### Parser Content
```Java
{
Name = microsoft-evsecurity-kv-endpoint-login-success-299
  Vendor = Microsoft
  Product = Event Viewer - Security
  ParserVersion = "v1.0.0"
  TimeFormat = "MM/dd/yyyy HH:mm:ss a"
  Conditions = [ """SourceName =AD FS Auditing""", """EventCode=299""" ]
  Fields = [
    """({time}\d\d\/\d\d\/\d\d\d\d \d\d:\d\d:\d\d (AM|am|PM|pm))""",
    """ComputerName =({host}[\w\-.]+)""",
    """EventCode=({event_code}\d+)""",
    """Relying party:\s*({service_name}[^\s]+)""",
    """Instance ID:\s*({iid}[^\s]+)""",
  ]


}
```