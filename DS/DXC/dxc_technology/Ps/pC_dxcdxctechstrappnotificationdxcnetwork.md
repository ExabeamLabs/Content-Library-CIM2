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
    """\sSource:\s+\/({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  ]
  ParserVersion = "v1.0.0"


}
```