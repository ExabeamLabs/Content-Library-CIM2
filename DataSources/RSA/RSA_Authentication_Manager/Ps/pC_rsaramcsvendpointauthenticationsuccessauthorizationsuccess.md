#### Parser Content
```Java
{
Name = rsa-ram-csv-endpoint-authentication-success-authorizationsuccess
  Vendor = RSA
  Product = RSA Authentication Manager
  TimeFormat = "yyyy-MM-dd HH:mm:ss:SSS zzz"
  Conditions = [ """,Authorization Success,""" ]
  Fields = [
    """({time}\d\d\d\d-\d\d-\d\d\s+\d\d:\d\d:\d\d:\d+\s+\w+)""",
    """\s\d\d:\d\d:\d\d:\d+[^,]+\,([^,]*\,){3}(\s*|({user}[^,\s]+))\,([^,]*\,){6}(\s*|({src_ip}[A-Fa-f:\d.]+))\,(\s*|({src_port}\d+))\,(\s*|({dest_ip}[A-Fa-f:\d.]+))\,""",
    """({event_name}Authorization Success)""",
    """({result}Success)"""
  ]
  ParserVersion = "v1.0.0"


}
```