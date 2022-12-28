#### Parser Content
```Java
{
Name = citrix-waf-cef-http-request-success-netscaler
  Vendor = Citrix
  Product = Citrix Web App Firewall
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """CEF:""", """|Citrix|NetScaler|NS""", """|APPFW|APPFW_""" ]
  Fields = [
    """src=({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """geolocation=(Unknown|({location}[^=]+?))\s+\w+=""",
    """spt=({src_port}\d+)""",
    """method=({method}[^\s]+)""",
    """request=({url}[^\s]+)\smsg=""",
    """\smsg=\s*({additional_info}[^=]+?)\s+\w+=""",
    """\|APPFW\|({event_name}[^\|]+?)(\s*$|\|)""",
    """\scs4=({category}[^=]+?)\s\w+=""",
    """act=({action}[^$]+?)\s*$""",
    """\scs1=({rule}[^=]+?)\s\w+=""",
    """\scs2=({interface_in}[^=]+?)\s\w+="""
  ]
  ParserVersion = "v1.0.0"


}
```