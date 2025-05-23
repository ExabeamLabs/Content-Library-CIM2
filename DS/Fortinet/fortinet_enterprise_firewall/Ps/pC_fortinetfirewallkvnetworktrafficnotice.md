#### Parser Content
```Java
{
Name = fortinet-firewall-kv-network-traffic-notice
  Vendor = Fortinet
  Product = Fortinet Enterprise Firewall
  ParserVersion = v1.0.0
  TimeFormat = "epoch_sec"
  Conditions = [
"""type="""
""""traffic""""
"""action="""
"""service="""
"""date="""
]
  Fields = [
    """eventtime="*({time}\d{10})""",
    """\Wdevname=\"?({host}[^\"]+?)\"?(\s+\w+=|\s*$)""",
    """\Wsrcip="*({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """\Wdstip="*({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """\Wsrcport="*({src_port}\d+)""",
    """\Wdstport="*({dest_port}\d+)""",
    """\Wdstintf=\"+({dest_interface}[^\"]+)""",
    """\Wsrcintf=\"+({src_interface}[^\"]+)""",
    """\Wuser="\s*((?:host\/({src_host}[^"]+))|({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?)(@({domain}[^"]+))?)\s*"""",
    """\Wsentbyte=({bytes_out}\d+)""",
    """\Wrcvdbyte=({bytes_in}\d+)""",
    """\Waction=\"*({action}[^\"]+?)\"*(\s+\w+=|\s*$)""",
    """\Wsentpkt=({packets_sent}\d+)""",
    """policyid=({policy_id}\d+)""",
    """\Wproto=({protocol}\d+)""",
    """\Wservice="*({protocol}[^"\/\s-]+?)(\_\d{1,5})?"""",
    """\Wsrcintfrole=\"+(undefined|({src_interface_role}[^\"]+))\"+""",
    """\Wdstintfrole=\"+(undefined|({dest_interface_role}[^\"]+))\"+""",
    """\Wsrccountry="(Reserved|({src_country}[^"]+))"""",
    """\Wdstcountry="(Reserved|({dest_country}[^"]+))"""",
    """\Wtype=\"+({event_category}[^"]+)""",
    """\Wsubtype=\"({operation}[^"]+)""",
    """\ssrcmac="?({src_mac}([a-fA-F\d]{2}[-:]){5}[a-fA-F\d]{2})"?""",
    """\Wtz="?({tz}[+-]\d+)"""
    """\ssrcname=\"*({src_host}[\w\-.]+)\"*"""
    """\sdstname=\"*({dest_host}[\w\-.]+)\"*"""
    """policyname="({policy_name}[^"]+)""""
]
 DupFields = [ "bytes_in->bytes"]


}
```