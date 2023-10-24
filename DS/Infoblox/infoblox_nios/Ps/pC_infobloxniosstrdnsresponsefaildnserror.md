#### Parser Content
```Java
{
Name = infoblox-nios-str-dns-response-fail-dnserror
  Vendor = Infoblox
  Product = Infoblox NIOS
  ParserVersion = "v1.0.0"
  TimeFormat = "MMM dd HH:mm:ss yyyy"
  Conditions = [ """ named[""", """DNS format error""" ]
  Fields = [
    """\d\d:\d\d:\d\d ({host}[\w\-\.]+)""",
    """from\s({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(#?({src_port}\d+))?""",
    """for client\s({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(#?({dest_port}\d+))?"""
    """named\[\S+?:\s+({additional_info}[^"]+)"""
  ]


}
```