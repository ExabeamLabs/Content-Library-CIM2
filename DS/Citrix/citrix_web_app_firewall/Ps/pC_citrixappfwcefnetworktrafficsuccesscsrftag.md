#### Parser Content
```Java
{
Name = citrix-appfw-cef-network-traffic-success-csrftag
  ParserVersion = v1.0.0
  Product =  Citrix Web App Firewall
  Conditions = [ """CEF:""", """|Citrix|NetScaler|NS""", """|APPFW|APPFW_CSRF_TAG|""" ]

citrix-appfw-network-connection = {
    Vendor = Citrix
    TimeFormat = "yyyy-MM-dd HH:mm:ss"
    Fields = [
      """src=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
      """geolocation=(Unknown|({location}[^=]+?))\s+\w+=""",
      """spt=({src_port}\d+)""",
      """method=({method}[^\s]+)""",
      """request=({url}[^\s]+)\smsg=""",
      """\smsg=\s*({additional_info}[^=]+?)\s+\w+=""",
      """\|APPFW\|({event_name}[^\|]+)""",
      """\scs4=({category}[^=]+?)\s\w+=""",
      """act=({action}(not blocked)|([^=]+?)(\d+|"))"""
      """\scs1=({rule}[^=]+?)\s\w+=""",
      """\scs2=({interface_in}[^=]+?)\s\w+="""
    
}
```