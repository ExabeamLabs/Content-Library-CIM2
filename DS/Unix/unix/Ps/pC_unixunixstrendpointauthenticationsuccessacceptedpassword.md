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
    """ from ({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  ]
  DupFields = [ "host->dest_host" ]


}
```