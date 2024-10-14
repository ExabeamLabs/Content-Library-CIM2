#### Parser Content
```Java
{
Name = fortinet-firewall-kv-network-traffic-success-accept
  Vendor = Fortinet
  Product = Fortinet Enterprise Firewall
  ParserVersion = v1.0.0
  TimeFormat = "yyyy-MM-dd 'time='HH:mm:ss"
  Conditions = [ 
""" vd="""
""" devname="""
""" devid="""
""" logid="""
""" level="""
"""action=accept"""
]
  Fields = [
    """date=({time}\d\d\d\d-\d\d-\d\d time=\d\d:\d\d:\d\d)""",
    """\slevel=\"*({severity}[^\s"]*)\"*""",
   """\sdevname=\"*({host}[^\s"]*)\"*""",
    """\saction=\"*({action}[^\s"]*)\"*""",
    """\sdstip="*({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """\ssrcip="*({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """\ssrcintf=\"?({src_interface}.+?)\"?\s+(\w+=|$)""",
    """\ssentbyte=({bytes_out}\d+)""",
    """\srcvdbyte=({bytes_in}\d+)""",
    """\sproto=({protocol}[^\s]*)""",
    """\sdstintf=\"?({dest_interface}.+?)\"?\s+(\w+=|$)""",
    """\sdstcountry=\"?({dest_country}.+?)\"?\s+(\w+=|$)""",
    """\ssrcport=({src_port}\d+)""",
    """\sdstport=({dest_port}\d+)""",
    """\ssrccountry=\"?({src_country}.+?)\"?\s+(\w+=|$)""",
    """\suser=\"?({user}[\w\.\-\!\#\^\~]{1,40}\$?)\"?\s+(\w+=|$)""",
    """\stransport=({src_translated_port}\d+)""",
    """\stransip=({src_translated_ip}[a-fA-F\d.:]+)""",
    """\smsg=\"*({additional_info}[^\s"]*)\"*""",
    """\slogdesc=\"*({event_name}[^\s"]*)\"*""",
    """\stranport=({src_translated_port}\d+)""",
    """\stranip=({dest_translated_ip}[a-fA-F\d.:]+)""",
    """\ssrcname=\"*({src_host}[^\s"]*)\"*""",
    """\Wtz="?({tz}[+-]\d+)"""
  ]


}
```