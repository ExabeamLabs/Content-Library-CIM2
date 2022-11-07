#### Parser Content
```Java
{
Name = fortinet-firewall-kv-network-traffic-success-vpn
  Vendor = Fortinet
  Product = Fortinet Enterprise Firewall
  ParserVersion = v1.0.0
  TimeFormat = "yyyy-MM-dd 'time='HH:mm:ssZ"
  Conditions = [ 
"""type="event""""
"""subtype="vpn""""
]
  Fields = [
    """devname=\"*({host}[\w\-.]+)""",
    """date=({time}\d\d\d\d-\d\d-\d\d time=\d\d:\d\d:\d\d([+-]\d\d:\d\d)?)""",
    """\slevel=\"*({severity}[^\s"]*)\"*""",
    """\smsg=\"*({additional_info}[^"]*)\"*""",
    """\saction=\"*({action}[^\s"]*)\"*""",
    """\sremip=({dest_ip}[a-fA-F\d.:]+)""",
    """\slocip=({src_ip}[a-fA-F\d.:]+)""",
    """\sremport=({dest_port}\d+)""",
    """\slocport=({src_port}\d+)""",
    """\suser=\"(?:N\/A|({user}[^\s@"]+))\"""",
    """\suser=\"(?:N\/A|({email_address}[^\s@"]+@[^\s@"]+))\"""",
    """\sstatus=\"*({result}[^\s"]*)\"*""",
    """\sdir=\"*({direction}[^\s"]*)\"*"""
  ]


}
```