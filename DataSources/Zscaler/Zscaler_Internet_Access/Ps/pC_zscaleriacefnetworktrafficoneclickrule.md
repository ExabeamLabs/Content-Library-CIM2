#### Parser Content
```Java
{
Name = zscaler-ia-cef-network-traffic-oneclickrule
  Vendor = Zscaler
  Product = Zscaler Internet Access
  ParserVersion = v1.0.0
  TimeFormat = "MM dd yyyy HH:mm:ss"
  Conditions = [
"""CEF:""",
"""|Zscaler|NSSFWLog|""",
""" suid=""",
""" reason=""",
""" act="""
  ]
  Fields = [
    """rt=({time}\d+\s+\d+\s+\d\d\d\d\s+\d+:\d+:\d+)""",
    """suid=(({email_address}[^@]+@[^\s]+)|({user}[^\s]+))\s+""",
    """src=({src_ip}[A-Fa-f\d:.]+)""",
    """dst=({dest_ip}[A-Fa-f\d:.]+)""",
    """spt=({src_port}\d+)""",
    """dpt=({dest_port}\d+)""",
    """act=({action}\S+)""",
    """reason=({rule}[^=]+?)\s+destination""",
    """in=({bytes_in}\d+)""",
    """out=({bytes_out}\d+)""",
    """cat=(Miscellaneous or Unknown|({ip_category}[^=]+?))\s+(\w+=|$)"""
  ]


}
```