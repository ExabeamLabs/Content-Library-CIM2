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
    """at ({time}\d\d:\d\d:\d\d\s(CT|UTC|EDT)\s\w+\s\w+\s\d+\s\d\d\d\d)""",
    """Source:\s*({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """user:\s*(|\u0003|(({domain}[^\]\\]+)\\)?({user}[^\]]+))\]""",
    """Reason:\s*({failure_reason}[^\]]+)\]""",
    """({event_name}LOGIN_FAILED)"""
  ]


}
```