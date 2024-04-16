#### Parser Content
```Java
{
Name = f5-apm-str-vpn-success-clientinfo
    Vendor = F5
    Product = F5 Access Policy Manager
    TimeFormat = "yyyy-MM-dd HH:mm:ss"
    Conditions = [ """:Common:""", """Received client info""", """Hostname:""" ]
    Fields = [
      """:Common:({session_id}[^:]+)""",
      """Hostname:\s*({src_host}[\w\-.]+)\s+\w+:""",
      """Platform:\s*({os}[^\s]+)\s"""
    ]
    ParserVersion = "v1.0.0"


}
```