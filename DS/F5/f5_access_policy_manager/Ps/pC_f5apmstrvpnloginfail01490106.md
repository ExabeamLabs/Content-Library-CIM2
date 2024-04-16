#### Parser Content
```Java
{
Name = f5-apm-str-vpn-login-fail-01490106
  ParserVersion = v1.0.0
  Vendor = F5
  Product = F5 Access Policy Manager
  TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss.SSSZ", "yyyy-MM-dd'T'HH:mm:ss"]
  Conditions = [ 
"""01490106:4""" 
]
  Fields = [
    """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)"""
    """@timestamp"\s*:\s*"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z)""",
    """\sprincipal name:\s*({user}[\w\.\-]{1,40}\$?)(@({domain}.+?))?(\.\s+|\s+)({failure_reason}[^\.]+)"""
    """"\s*Error_Code="({failure_code}[^"]+)""""
  ]


}
```