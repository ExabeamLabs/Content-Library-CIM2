#### Parser Content
```Java
{
Name = unix-unix-str-endpoint-login-success-shelllogin
  Vendor = Unix
  Product = Unix
  TimeFormat = "MMM dd HH:mm:ss yyyy"
  Conditions = [ """logged in from """, """SHELL_LOGIN: """ ]
  Fields = [
    """({time}\w+\s+\d+ \d\d:\d\d:\d\d \d\d\d\d)""",
    """\d\d:\d\d:\d\d \d\d\d\d ({host}[^\s]+)""",
    """({event_name}SHELL_LOGIN)""",
    """SHELL_LOGIN: ({user}[^\s]+)""",
    """logged in from ({src_ip}[a-fA-F:\d\.]+)\."""
  ]
  DupFields = [ "host->dest_host" ]
  ParserVersion = "v1.0.0"


}
```