#### Parser Content
```Java
{
Name = f5-bigip-kv-app-notification-success-vpn
  Vendor = F5
  Product = F5 BIG-IP
  ParserVersion = "v1.0.0"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ"
  Conditions = [ """"VPN"""", """errdefs_msgno="""", """endpoint software detected""" ]
  Fields = [
    """({time}\d{4}-\d{2}-\d{2}T\d{2}:\d{2}:\d{2}\.\d{6}(\+|-)\d{2}:\d{2})\s({host}[\w.-]+)""",
    """endpoint software detected \(({additional_info}[^\)]+)\)""",
    """({event_name}endpoint software detected)"""
  ]


}
```