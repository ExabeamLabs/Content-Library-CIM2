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
    """TCP ({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}):({src_port}\d+) -> ({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}):({dest_port}\d+)""",
    """({protocol}SSL)""",
  ]


}
```