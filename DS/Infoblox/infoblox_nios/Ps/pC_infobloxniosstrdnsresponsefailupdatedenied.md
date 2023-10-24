#### Parser Content
```Java
{
Name = infoblox-nios-str-dns-response-fail-updatedenied
  Vendor = Infoblox
  Product = Infoblox NIOS
  ParserVersion = "v1.0.0"
  TimeFormat = "MMM dd HH:mm:ss yyyy"
  Conditions = [ """ named[""", """ update """, """ denied""" ]
  Fields = [
    """\d\d:\d\d:\d\d ({host}[\w\-\.]+)""",
    """\s*({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(#({src_port}\d+))"""
    """({action}denied)"""
    """named\[\S+?:\s+({additional_info}[^~]+?)\s*$"""
  ]


}
```