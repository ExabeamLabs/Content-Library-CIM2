#### Parser Content
```Java
{
Name = f5-waf-str-network-traffic-fail-ssl
  Vendor = F5
  Product = F5 Advanced Web Application Firewall
  ParserVersion = v1.0.0
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ 
""" tmm"""
""" SSL """
"""No shared ciphers between SSL peers""" 
]
  Fields = [
    """\d\d:\d\d:\d\d ({host}[^\s]+)""",
    """peers ({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))\.({src_port}\d+):({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))\.({dest_port}\d+)""",
    """({event_name}No shared ciphers between SSL peers)""",
    """({protocol}SSL)"""
  ]
  DupFields = [ "event_name->failure_reason" ]


}
```