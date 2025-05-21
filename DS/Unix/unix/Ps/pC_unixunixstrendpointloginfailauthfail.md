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
    """Authentication failed for ({user}[\w\.\-\!\#\^\~]{1,40}\$?) from ({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """because of ({failure_reason}[^.]+)\s+"""
  ]
  ParserVersion = "v1.0.0"
  DupFields = [ "host->dest_host" ]


}
```