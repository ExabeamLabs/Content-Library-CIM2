#### Parser Content
```Java
{
Name = dxc-dxctech-str-app-notification-dxcnetwork
  Vendor = DXC
  Product = DXC Technology
  TimeFormat = "MMM dd HH:mm:ss yyyy"
  Conditions = [ """TAG: DXC Network""" ]
  Fields = [
    """({time}\w+ \d+ \d\d:\d\d:\d\d \d{4})\s+({host}[^\s]+)""",
    """\sSource:\s+\/({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})"""
  ]
  ParserVersion = "v1.0.0"


}
```