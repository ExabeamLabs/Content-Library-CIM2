#### Parser Content
```Java
{
Name = attivo-botsink-cef-network-traffic-success-networktrafficsuccess
  ParserVersion = v1.0.0
  Vendor = Attivo
  Product = BOTsink
  TimeFormat = "epoch"
  Conditions = [ """CEF:""", """|Attivo|BOTsink|""", """dIPDomain="""]
  Fields = [
    """rt=({time}\d+)""",
    """\d\d:\d\d:\d\d\s({host}[^\s]*)\s""",
    """dvc=({host}[A-Fa-f:\d.]+)""",
    """dst=({dest_ip}[A-Fa-f:\d.]+)""",
    """src=({src_ip}[A-Fa-f:\d.]+)""",
    """smac=({src_mac}(\w{2}:){5}\w{2})""",
    """(dpt|dst_port_list)=({dest_port}\d+)""",
    """dIPDomain=({web_domain}[^\s]+)""",
    """spt=({src_port}\d+)""",
    """shost=({src_host}[\w\-.]+)""",
    """dhost=({dest_host}[\w\-.]+)""",
    """Interface\\?=({src_interface}[^\s]+)""",
    """msg=\s*({rule}.+?)\s+(\w+=|$)""",
    """({direction}Inbound)""",
    """({protocol}RDP|TCP|tcp)""",
    """CEF:([^\|]*\|){5}\s*({operation}[^\|]*?)\s*\|""",
   ]


}
```