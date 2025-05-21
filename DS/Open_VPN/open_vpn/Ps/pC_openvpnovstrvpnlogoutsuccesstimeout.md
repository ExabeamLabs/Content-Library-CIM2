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
    """openvpn\[[^\]]+\]\:\s(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\/({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))\:({src_port}\d+)""",
    """({event_name}Inactivity timeout)""",
    """Inactivity timeout\s({additional_info}[^\"]+?)\s*("|$)"""
  ]


}
```