#### Parser Content
```Java
{
Name = openvpn-ov-str-vpn-logout-success-timeout
  ParserVersion = v1.0.0
  Vendor = Open VPN
  Product = Open VPN
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ 
"""openvpn"""
"""Inactivity timeout""" 
]
  Fields = [
    """openvpn\[({process_id}[^\]]+)\]""",
    """openvpn\[[^\]]+\]\:\s({user}[^\/]+)\/({src_ip}[a-fA-F\d.:]+)\:({src_port}\d+)""",
    """({event_name}Inactivity timeout)""",
    """Inactivity timeout\s({additional_info}[^\"]+?)\s*("|$)"""
  ]


}
```