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
    """rt=({time}\d{13})""",
    """\d\d:\d\d:\d\d\s({host}[^\s]*)\s""",
    """dvc=({host}[A-Fa-f:\d.]+)""",
    """dst=({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """src=({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
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