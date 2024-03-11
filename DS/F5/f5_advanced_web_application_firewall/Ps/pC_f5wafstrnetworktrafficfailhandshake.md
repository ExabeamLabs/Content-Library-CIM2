#### Parser Content
```Java
{
Name = f5-waf-str-network-traffic-fail-handshake
  Vendor = F5
  Product = F5 Advanced Web Application Firewall
  ParserVersion = v1.0.0
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ 
""" tmm"""
""" SSL """
"""SSL Handshake failed""" 
]
  Fields = [
    """\d\d:\d\d:\d\d ({host}[^\s]+)""",
    """({event_name}SSL Handshake failed)""",
    """TCP ({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})):({src_port}\d+) -> ({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})):({dest_port}\d+)""",
    """({protocol}SSL)""",
  ]


}
```