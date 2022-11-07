#### Parser Content
```Java
{
Name = fortinet-vpn-cef-vpn-logout-success-connection
  ParserVersion = v1.0.0
  Vendor = Fortinet
  Product = VPN
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ 
"""IPsec connection status change"""
"""tunnel-down"""
"""user="""
]
  Fields = [
    """date=({time}\d\d\d\d-\d\d-\d\d[\s,]*time=\d\d:\d\d:\d\d)""",
    """devname="*({host}[^\s",]+)""",
    """\d\s({host}[^\s]+)\sdate=""",
    """rem_?ip=(?:N\/A|({src_ip}[^\s,]+))[\s,]""",
    """xauth_?user="(?:N\/A|({user}[^"]+))"""",
    """(rcvd|rcvdbyte)=({bytes_out}\d+)""",
    """(sent|sentbyte)=({bytes_in}\d+)"""
  ]


}
```