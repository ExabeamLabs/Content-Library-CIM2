#### Parser Content
```Java
{
Name = f5-apm-str-vpn-success-statistics
  Vendor = F5
  Product = F5 Access Policy Manager
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """:Common:""", """/Common/""", """Session statistics -""" ]
  Fields = [
    """:Common:({session_id}[^:]+)""",
    """Session statistics - bytes in:\s*({bytes_in}\d+),\s+bytes out:\s*({bytes_out}\d+)"""
  ]
  ParserVersion = "v1.0.0"


}
```