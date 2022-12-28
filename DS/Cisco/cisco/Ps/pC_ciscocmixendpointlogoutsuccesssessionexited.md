#### Parser Content
```Java
{
Name = cisco-c-mix-endpoint-logout-success-sessionexited
  Vendor = Cisco
  Product = Cisco
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  ParserVersion = "v1.0.0"
  Conditions = [ """-LOGOUT: """, """has exited tty session""" ]
  Fields = [
    """<\d+>[^:\s]+:\s+({host}[^:\s]+):""",
    """({event_code}\S+\d+-LOGOUT):""",
    """User\s*({user}\S+)\s+has exited tty session""",
    """\(({src_ip}[a-fA-F\d.:]+)\)\s*$""",
  ] 


}
```