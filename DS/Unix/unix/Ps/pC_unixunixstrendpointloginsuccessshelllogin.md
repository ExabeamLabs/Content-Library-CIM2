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
    """\d\d:\d\d:\d\d \d\d\d\d ({dest_host}({host}[^\s]+))""",
    """({event_name}SHELL_LOGIN)""",
    """SHELL_LOGIN: ({user}[\w\.\-\!\#\^\~]{1,40}\$?)""",
    """logged in from ({src_ip}[a-fA-F:\d\.]+)\."""
  ]
  ParserVersion = "v1.0.0"


}
```