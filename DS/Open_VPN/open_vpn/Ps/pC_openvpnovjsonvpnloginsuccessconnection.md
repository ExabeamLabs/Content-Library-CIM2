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
    """ openvpn\[\d+\]:\s+(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[^\s\/]+))\/({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})):({src_port}\d+)""",
    """IPv4=({src_translated_ip}[A-Fa-f:\d.]+)""",
    """hostname":"({host}[^"]+)"""
  ]
  DupFields = [ "user->account" ]


}
```