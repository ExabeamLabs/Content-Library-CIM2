#### Parser Content
```Java
{
Name = openvpn-ov-str-vpn-logout-success-reset
  ParserVersion = v1.0.0
  Vendor = Open VPN
  Product = Open VPN
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
  Conditions = [
"""Connection reset, restarting"""
"""openvpn""" 
]
  Fields = [
    """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d(\+|\-)\d+)""",
    """(Jan|Feb|Mar|Apr|May|Jun|Jul|Aug|Sep|Oct|Nov|Dec)\s\W?\d+\s\d+:\d+:\d+\s\d+\s({user}[\w\.\-\!\#\^\~]{1,40}\$?)\/({src_ip}\d{1,3}.\d{1,3}.\d{1,3}.\d{1,3}):({src_port}\d+)""",
    """({additional_info}Connection reset, restarting)"""
  ]


}
```