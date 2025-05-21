#### Parser Content
```Java
{
Name = openvpn-ov-json-vpn-login-success-connection
  ParserVersion = v1.0.0
  Vendor = Open VPN
  Product = Open VPN
  ExtractionType = json
  TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss.SSSZ", "MMM dd HH:mm:ss"]
  Conditions = [ 
""" openvpn[""" 
"""MULTI_sva: pool returned """
"""IPv4=""" 
]
  Fields = [
    """({time}\w+\s+\d+ \d+:\d+:\d+)"""
    """"@timestamp":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\dZ)""",
    """ openvpn\[\d+\]:\s+(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\/({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})):({src_port}\d+)""",
    """IPv4=({src_translated_ip}[A-Fa-f:\d.]+)""",
    """hostname":"({host}[^"]+)""",
    """exa_json_path=$.@timestamp,exa_field_name=time""",
    """exa_regex= openvpn\[\d+\]:\s+(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\/({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})):({src_port}\d+)""",
    """exa_regex=IPv4=({src_translated_ip}[A-Fa-f:\d.]+)""",
    """exa_json_path=$.beat.hostname,exa_field_name=host"""
  ]
  DupFields = [ "user->account" ]


}
```