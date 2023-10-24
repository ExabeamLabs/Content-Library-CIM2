#### Parser Content
```Java
{
Name = "f5-apm-json-endpoint-login-fail-01490212"
  Vendor = F5
  Product = F5 Access Policy Manager
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [ """01490212:4""" ]
  Fields = [
    """@timestamp"\s*:\s*"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z)""",
    """authenticate with '({user}[\w\.\-]{1,40}\$?)' failed""",
  ]
  ParserVersion = "v1.0.0"


}
```