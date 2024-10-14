#### Parser Content
```Java
{
Name = fortinet-vpn-cef-vpn-logout-success-connection
  ParserVersion = v1.0.0
  Vendor = Fortinet
  Product = FortiGate
  TimeFormat = ["yyyy-MM-dd' time='HH:mm:ss","yyyy-MM-dd',time='HH:mm:ss"]
  time_createdFormat = ["yyyy-MM-dd HH:mm:ss"]
  time_modifiedFormat = ["yyyy-MM-dd HH:mm:ss"]
  Conditions = [ 
"""IPsec connection status change"""
"""tunnel-down"""
"""user="""
]
  Fields = [
    """date=({time}\d\d\d\d-\d\d-\d\d[\s,]*time=\d\d:\d\d:\d\d)""",
    """devname="*({host}[^\s",]+)""",
    """\d\s({host}[^\s]+)\sdate=""",
    """rem_?ip=(?:N\/A|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)[\s,]""",
    """xauth_?user="(?:N\/A|({email_address}[^@"]+@[^\."]+\.[^"]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""",
    """(rcvd|rcvdbyte)=({bytes_out}\d+)""",
    """(sent|sentbyte)=({bytes_in}\d+)""",
    """\Wtz="?({tz}[+-]\d+)"""
  ]


}
```