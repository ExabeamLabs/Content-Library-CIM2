#### Parser Content
```Java
{
Name = cisco-ise-kv-endpoint-login-fail-loginfailed
  ParserVersion = "v1.0.0"
  Vendor = Cisco
  Product = Cisco ISE
  TimeFormat = "HH:mm:ss 'CT' EEE MMM d yyyy"
  Conditions = [ """LOGIN_FAILED:""", """Login failed [user:""", """[Source:""", """[localport: """]
  Fields = [
    """at ({time}\d\d:\d\d:\d\d\s(CT|UTC)\s\w+\s\w+\s\d+\s\d\d\d\d)""",
    """Source:\s*({src_ip}[a-fA-F\d:.]+)""",
    """user:\s*(|\u0003|({user}[^\]]+))\]""",
    """Reason:\s*({failure_reason}[^\]]+)\]""",
    """({event_name}LOGIN_FAILED)"""
  ]


}
```