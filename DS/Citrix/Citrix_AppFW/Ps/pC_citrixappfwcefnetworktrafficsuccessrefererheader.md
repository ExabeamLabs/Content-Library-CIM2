#### Parser Content
```Java
{
Name = citrix-appfw-cef-network-traffic-success-refererheader
  ParserVersion = v1.0.0
  Product =  Citrix AppFW
  Conditions = [ """CEF:""", """|Citrix|NetScaler|NS""", """|APPFW|APPFW_REFERER_HEADER|""" ]

citrix-appfw-network-connection = {
    Vendor = Citrix
    TimeFormat = "yyyy-MM-dd HH:mm:ss"
    Fields = [
      """src=({src_ip}[a-fA-F\d:.]+)""",
      """geolocation=(Unknown|({location}[^=]+?))\s+\w+=""",
      """spt=({src_port}\d+)""",
      """method=({method}[^\s]+)""",
      """request=({url}[^\s]+)\smsg=""",
      """\smsg=\s*({additional_info}[^=]+?)\s+\w+=""",
      """\|APPFW\|({event_name}[^\|]+)""",
      """\scs4=({category}[^=]+?)\s\w+=""",
      """act=({action}[^$]+?)\s*$""",
      """\scs1=({rule}[^=]+?)\s\w+=""",
      """\scs2=({interface_in}[^=]+?)\s\w+="""
    
}
```