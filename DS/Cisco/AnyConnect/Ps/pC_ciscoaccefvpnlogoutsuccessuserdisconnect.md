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
  """\srt=({time}\d+)"""
  """\ssourceTranslatedAddress=({src_ip}[^\s]+)"""
  """\sduser=(?:({domain}[^\s]+?)\\+)?({user}.+?)\s+(\w+=|$)"""
  """\sdvc=({dest_ip}[^\s]+)"""
  """\sdvc=({host}[^\s]+)"""
  """\sdvchost=({dest_host}[^\s]+)"""
  """\sdvchost=({host}[^\s]+)"""
]
ParserVersion = "v1.0.0"


}
```