#### Parser Content
```Java
{
Name = unix-unix-str-endpoint-login-fail-failedtologin
  ParserVersion = v1.0.0
  Vendor = Unix
  Product = Unix
  TimeFormat = "MMM dd HH:mm:ss yyyy"
  Conditions = [ """SSHS_VERSION_MISMATCH: """, """SSH client """, """failed to log in """ ]
  Fields = [
    """({time}\w+\s+\d+ \d\d:\d\d:\d\d \d\d\d\d)""",
    """\d\d:\d\d:\d\d(\.\S+)? \d\d\d\d ({host}[^\s]+)""",
    """({event_name}SSHS_VERSION_MISMATCH)""",
    """SSH client ({src_ip}[a-fA-F:\d\.]+) ({failure_reason}[^.]+)"""
  ]
  DupFields = [ "host->dest_host" ]


}
```