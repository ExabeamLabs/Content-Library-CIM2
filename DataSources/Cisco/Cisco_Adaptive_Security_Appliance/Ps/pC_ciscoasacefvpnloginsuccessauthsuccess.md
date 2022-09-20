#### Parser Content
```Java
{
Name = cisco-asa-cef-vpn-login-success-authsuccess
Vendor = "Cisco"
Product = "Cisco Adaptive Security Appliance"
TimeFormat = "epoch"
Conditions = [
  """CEF:"""
  """|CISCO|FWSM|"""
  """|Authentication succeeded|"""
]
Fields = [
  """\srt=({time}\d+)"""
  """\ssrc=({src_translated_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})"""
  """\ssuser=({user}.+?)\s+\w+="""
  """\sdst=({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})"""
  """\sdvc=({host}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})"""
  """\sdvchost=({host}[^\s]+)"""
]
DupFields = [
  "user->account"
]
ParserVersion = "v1.0.0"


}
```