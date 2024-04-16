#### Parser Content
```Java
{
Name = "catonetwork-cc-cef-vpn-http-success-security"
Vendor = "CatoNetworks"
Product = "Cato Cloud"
TimeFormat = "EEE MMM dd HH:mm:ss Z yyyy"
Conditions = [
  """CEF:"""
  """|CatoNetworks|"""
  """internalType=SECURITY"""
  """ act="""
]
Fields = [
    """\Wrt=({time}\w+\s+\w+\s+\d+\s+\d\d:\d\d:\d\d\s+\w+\s+\d\d\d\d)""",
    """\Wcs1=({src_country}[^=]+?)\s+(\w+=|$)""",
    """\Wcs2=(-|({dest_country}[^=]+?))\s+(\w+=|$)""",
    """\Wdst=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """\Wsrc=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """\Wdpt=({dest_port}\d+)""",
    """\Wdproc=({categories}({event_category}[^,;\=]+)[^\=]*?)\s+(\w+=|$)""",
    """\Wact=({action}[^=]+?)\s+(\w+=|$)""",
    """destinationDnsDomain=({web_domain}[^=]+?)\s\w+=""",
    """\Wshost=({full_name}[^=]+?)\s+(\w+=|$)""",
    """\Wsuser=({src_host}[\w\-.]+)""",
    """user_email=({email_address}[^@]+@[^=]+?)\s\w+="""
]
ParserVersion = "v1.0.0"


}
```