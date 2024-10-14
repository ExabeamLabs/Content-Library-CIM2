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
    """Client IP:\s*({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """Error message:\s*(({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.-])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))-The user name""",
    """Error message:\s*({failure_reason}.+?)\s+Exception details:"""
  ]


}
```