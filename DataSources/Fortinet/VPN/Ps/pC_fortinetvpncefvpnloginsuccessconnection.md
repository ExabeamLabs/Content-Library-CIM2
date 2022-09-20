#### Parser Content
```Java
{
Name = fortinet-vpn-cef-vpn-login-success-connection
  ParserVersion = v1.0.0
  Vendor = Fortinet
  Product = VPN
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ 
"""IPsec connection status change""" 
"""tunnel-up"""
"""user=""" 
]
  Fields = [
    """devname="*({host}[^\s"]+)""",
    """\d\s({host}[^\s]+)\sdate=""",
    """rem_?ip=({src_ip}[^\s,]+)[\s,]""",
    """tunnel_?ip=(?:N\/A|({src_translated_ip}[^\s,]+))[\s,]""",
    """xauth_?user="+(?:N\/A|({user}[^"]+))"""",
    """(\s|,)group="+(?:N\/A|({realm}[^"]+))"""
  ]
  DupFields = ["user->account"]


}
```