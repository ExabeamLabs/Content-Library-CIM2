#### Parser Content
```Java
{
Name = openvpn-ov-json-vpn-login-success-connection
  ParserVersion = v1.0.0
  Vendor = Open VPN
  Product = Open VPN
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [ 
""" openvpn[""" 
"""MULTI_sva: pool returned """
"""IPv4=""" 
]
  Fields = [
    """"@timestamp":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\dZ)""",
    """ openvpn\[\d+\]:\s+({user}[^\s\/]+)\/({src_ip}[A-Fa-f:\d.]+):({src_port}\d+)""",
    """IPv4=({src_translated_ip}[A-Fa-f:\d.]+)""",
    """hostname":"({host}[^"]+)"""
  ]
  DupFields = [ "user->account" ]


}
```