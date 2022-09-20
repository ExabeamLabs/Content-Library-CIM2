#### Parser Content
```Java
{
Name = fortinet-vpn-cef-vpn-logout-success-down
  ParserVersion = v1.0.0
  Vendor = Fortinet
  Product = VPN
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ 
"""action="tunnel-down""""
"""subtype="vpn""""
]
  Fields = [
    """({time}\d\d\d\d\/\d\d\/\d\d \d\d:\d\d:\d\d),[^,]*,({host}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})""",
    """date=({time}\d\d\d\d-\d\d-\d\d time=\d\d:\d\d:\d\d([+-]\d\d:\d\d)?)""",
    """\Wdevname="+({host}[\w\-.]+)""",
    """\Wremip=({src_ip}[A-Fa-f:\d.]+)""",
    """\Wtunnelip=(\(null\)|({src_translated_ip}[A-Fa-f:\d.]+))""",
    """\Wuser="(.+?\\\\)?(?:N\/A|({user}[^\s@"]+))"""",
    """\Wuser="N\/A|({email_address}[^\s@"]+@[^\s@"]+)"""",
    """\Wmsg="+({event_name}[\w\s]+)"""",
    """\Wsentbyte=({bytes_out}\d+)""",
    """\Wrcvdbyte=({bytes_in}\d+)""",
    """\Wgroup="+({realm}[^"]+)"""
  ]
  DupFields = [ "host->dest_host", "user->account" ]


}
```