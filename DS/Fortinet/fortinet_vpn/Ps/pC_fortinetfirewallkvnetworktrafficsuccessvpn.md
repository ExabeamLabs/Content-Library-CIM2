#### Parser Content
```Java
{
Name = fortinet-firewall-kv-network-traffic-success-vpn
  Vendor = Fortinet
  Product = Fortinet VPN
  ParserVersion = v1.0.0
  TimeFormat = "yyyy-MM-dd 'time='HH:mm:ss"
  Conditions = [ 
"""type="event""""
"""subtype="vpn""""
]
  Fields = [
    """devname=\"*({host}[\w\-.]+)""",
    """date=({time}\d\d\d\d-\d\d-\d\d time=\d\d:\d\d:\d\d)""",
    """\slevel=\"*({severity}[^\s"]*)\"*""",
    """\smsg=\"*({additional_info}[^"]*)\"*""",
    """\saction=\"*({action}[^\s"]*)\"*""",
    """\sremip=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """\slocip=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """\sremport=({dest_port}\d+)""",
    """\slocport=({src_port}\d+)""",
    """\suser=\"(?:N\/A|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\"""",
    """\suser="(?:N\/A|({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+))"""",
    """\sstatus=\"*({result}[^\s"]*)\"*""",
    """\sdir=\"*({direction}[^\s"]*)\"*""",
    """\Wsentbyte=({bytes_out}\d+)""",
    """\srcvdbyte=({bytes_in}\d+)""",
    """\Wtz="?({tz}[+-]\d+)"""
  ]


}
```