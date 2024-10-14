#### Parser Content
```Java
{
Name = fortinet-vpn-cef-vpn-login-success-connection
  ParserVersion = v1.0.0
  Vendor = Fortinet
  Product = FortiGate
  TimeFormat = "yyyy-MM-dd' time='HH:mm:ss"
  Conditions = [ 
"""IPsec connection status change""" 
"""tunnel-up"""
"""user=""" 
]
  Fields = [
    """devname="*({host}[^\s"]+)""",
    """\d\s({host}[^\s]+)\sdate=""",
    """loc_?ip=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?[\s,]""",
    """rem_?ip=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?[\s,]""",
    """tunnel_?ip=(?:N\/A|({src_translated_ip}[^\s,]+))[\s,]""",
    """xauth_?user="+(?:N\/A|({email_address}[^@"]+@[^\."]+\.[^"]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""",
    """(\s|,)group="+(?:N\/A|({realm}[^"]+))"""
    """({time}\d\d\d\d-\d\d-\d\d\s+time=\d\d:\d\d:\d\d)""",
    """\Wtz="?({tz}[+-]\d+)"""
  ]
  DupFields = ["user->account"]


}
```