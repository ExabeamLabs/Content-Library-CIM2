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
    """\d\d:\d\d:\d\d \d\d\d\d ({dest_host}({host}[^\s]+))""",
    """({event_name}SSHS_CONNECT)""",
    """SSHS_CONNECT: ({user}[\w\.\-\!\#\^\~]{1,40}\$?)""",
    """IP: ({src_ip}[a-fA-F:\d\.]+)\)"""
  ]
  ParserVersion = "v1.0.0"


}
```