#### Parser Content
```Java
{
Name = zscaler-ia-cef-network-traffic-blocked
  Vendor = Zscaler
  Product = Zscaler Internet Access
  ParserVersion = v1.0.0
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [
"""CEF:""",
"""|Zscaler|NSSFWlog|""",
""" reason=""",
""" act=""",
""" suser="""
  ]
  Fields = [
    """suser=(({email_address}[^=@]+@[^\.\s]+\.[^=]+?)|({user}[^=]+?))\s+\w+=""",
    """src=({src_ip}[A-Fa-f\d:.]+)""",
    """dst=({dest_ip}[A-Fa-f\d:.]+)""",
    """spt=({src_port}\d+)""",
    """dpt=({dest_port}\d+)""",
    """(?i)\sact=({action}(Allow|Drop))""",
    """sourceTranslatedAddress=({src_translated_ip}[A-Fa-f:.\d]+)""",
    """destinationTranslatedAddress=({dest_translated_ip}[A-Fa-f:.\d]+)""",
    """proto=({protocol}[^=]+?)\s\w+=""",
    """deviceDirection=({direction}\d)""",
    """reason=({rule}[^=]+?)\s+\w+=""",
    """in=({bytes_in}\d+)""",
    """out=({bytes_out}\d+)"""
  ]


}
```