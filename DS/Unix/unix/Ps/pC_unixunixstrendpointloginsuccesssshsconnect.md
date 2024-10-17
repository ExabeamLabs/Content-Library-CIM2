#### Parser Content
```Java
{
Name = unix-unix-str-endpoint-login-success-sshsconnect
  Vendor = Unix
  Product = Unix
  TimeFormat = "MMM dd HH:mm:ss yyyy"
  Conditions = [ """SSH user""", """connected to """, """SSHS_CONNECT: """ ]
  Fields = [
    """({time}\w+\s+\d+ \d\d:\d\d:\d\d \d\d\d\d)""",
    """\d\d:\d\d:\d\d \d\d\d\d ({host}[^\s]+)""",
    """({event_name}SSHS_CONNECT)""",
    """SSHS_CONNECT: ({user}[\w\.\-\!\#\^\~]{1,40}\$?)""",
    """IP: ({src_ip}[a-fA-F:\d\.]+)\)"""
  ]
  DupFields = [ "host->dest_host" ]
  ParserVersion = "v1.0.0"


}
```