#### Parser Content
```Java
{
Name = cisco-ac-cef-vpn-logout-success-userdisconnect
Vendor = "Cisco"
Product = "AnyConnect"
TimeFormat = "epoch"
Conditions = [
  """CEF:"""
  """|CISCO|Cisco VPN|"""
  """|User disconnected|"""
]
Fields = [
  """\srt=({time}\d{13})"""
  """\ssourceTranslatedAddress=({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  """\sduser=(?:({domain}[^\s]+?)\\+)?({user}.+?)\s+(\w+=|$)"""
  """\sdvc=({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
  """\sdvc=({host}[^\s]+)"""
  """\sdvchost=({dest_host}[^\s]+)"""
  """\sdvchost=({host}[^\s]+)"""
]
ParserVersion = "v1.0.0"


}
```