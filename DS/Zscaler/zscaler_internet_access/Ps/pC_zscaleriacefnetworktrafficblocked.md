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
    """suser=(({email_address}[^=@]+@[^\.\s]+\.[^=]+?)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s+\w+=""",
    """src=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """dst=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """spt=({src_port}\d+)""",
    """dpt=({dest_port}\d+)""",
    """(?i)\sact=({action}(Allow|Drop))""",
    """sourceTranslatedAddress=({src_translated_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))""",
    """destinationTranslatedAddress=({dest_translated_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))""",
    """proto=({protocol}[^=]+?)\s\w+=""",
    """deviceDirection=({direction}\d)""",
    """reason=({rule}[^=]+?)\s+\w+=""",
    """in=({bytes_in}\d+)""",
    """out=({bytes_out}\d+)"""
  ]


}
```