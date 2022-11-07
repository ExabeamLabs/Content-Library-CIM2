#### Parser Content
```Java
{
Name = unix-unix-str-endpoint-authentication-success-acceptedpassword
  ParserVersion = v1.0.0
  Vendor = Unix
  Product = Unix
  TimeFormat = "MMM dd HH:mm:ss yyyy"
  Conditions = [ """Accepted password for """, """ from """, """SSHS_LOG: """ ]
  Fields = [
    """({time}\w+\s+\d+ \d\d:\d\d:\d\d \d\d\d\d)""",
    """\d\d:\d\d:\d\d(\.\S+)? \d\d\d\d ({host}[^\s]+)""",
    """({event_name}SSHS_LOG)""",
    """Accepted password for ({user}[^\s]+)""",
    """ from ({src_ip}[a-fA-F:\d\.]+)"""
  ]
  DupFields = [ "host->dest_host" ]


}
```