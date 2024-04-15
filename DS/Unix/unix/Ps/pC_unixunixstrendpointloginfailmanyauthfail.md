#### Parser Content
```Java
{
Name = "unix-unix-str-endpoint-login-fail-manyauthfail"
  Vendor = "Unix"
  Product = "Unix"
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [
    """Disconnecting: Too many authentication failures for"""
  ]
  Fields = [
    """({host}[\w.\-]+)\s+sshd\["""
    """({event_name}Too many authentication failures) for ({user}\S+)"""
    """({event_code}ssh)"""
  ]
  ParserVersion = "v1.0.0"


}
```