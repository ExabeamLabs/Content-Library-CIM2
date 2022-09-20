#### Parser Content
```Java
{
Name = f5-waf-str-network-traffic-fail-ssl
  Vendor = F5
  Product = Advanced Web Application Firewall (WAF)
  ParserVersion = v1.0.0
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ 
""" tmm"""
""" SSL """
"""No shared ciphers between SSL peers""" 
]
  Fields = [
    """\d\d:\d\d:\d\d ({host}[^\s]+)""",
    """peers ({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})\.({src_port}\d+):({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})\.({dest_port}\d+)""",
    """({event_name}No shared ciphers between SSL peers)""",
    """({protocol}SSL)"""
  ]


}
```