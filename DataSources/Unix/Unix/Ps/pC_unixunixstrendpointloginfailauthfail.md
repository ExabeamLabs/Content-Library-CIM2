#### Parser Content
```Java
{
Name = unix-unix-str-endpoint-login-fail-authfail
  Vendor = Unix
  Product = Unix
  TimeFormat = "MMM dd HH:mm:ss yyyy"
  Conditions = [ """Authentication failed for""", """ from """, """SSHS_LOG: """ ]
  Fields = [
    """({time}\w+\s+\d+ \d\d:\d\d:\d\d \d\d\d\d)""",
    """\d\d:\d\d:\d\d \d\d\d\d ({host}[^\s]+)""",
    """({event_name}SSHS_LOG)""",
    """Authentication failed for ({user}[^\s]+) from ({src_ip}[a-fA-F:\d\.]+)""",
    """because of ({failure_reason}[^.]+)\s+"""
  ]
  ParserVersion = "v1.0.0"
  DupFields = [ "host->dest_host" ]


}
```