#### Parser Content
```Java
{
Name = unix-unix-kv-endpoint-authentication-pam
  Vendor = Unix
  Product = Unix
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """pam_""", """ httpd: """, """(httpd:auth):""", """: authentication""", """tty=""" ]
  Fields = [
    """({host}[\w\-.]+)\s+httpd:""",
    """\Wuser=({user}[\w\.\-]{1,40}\$?)(\s+\w+=|\s*$)""",
    """\Wrhost=(|(({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})|({src_host}[\w\-.]+)))\s""",
    """pam_(sss|unix)\(httpd:auth\):\s+authentication\s+({result}success|failure);""",
    """({event_code}httpd)""",
  ]
  ParserVersion = "v1.0.0"


}
```