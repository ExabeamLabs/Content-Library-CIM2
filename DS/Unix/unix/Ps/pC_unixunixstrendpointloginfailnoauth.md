#### Parser Content
```Java
{
Name = "unix-unix-str-endpoint-login-fail-noauth"
  Vendor = "Unix"
  Product = "Unix"
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [
    """ sshd["""
    """]: No authentication methods succeeded for user"""
  ]
  Fields = [
    """\w+\s+\d+\s+\d+:\d+:\d+\s+({host}[\w\-.]+)\s+"""
    """No authentication methods succeeded for user ({user}[^\"\"]+)"""
  ]
  ParserVersion = "v1.0.0"


}
```