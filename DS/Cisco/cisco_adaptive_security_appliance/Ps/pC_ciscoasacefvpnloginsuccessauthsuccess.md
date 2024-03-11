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
  """\srt=({time}\d{13})"""
  """\ssrc=({src_translated_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})"""
  """\ssuser=({user}.+?)\s+\w+="""
  """\sdst=({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
  """\sdvc=({host}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})"""
  """\sdvchost=({host}[^\s]+)"""
]
DupFields = [
  "user->account"
]
ParserVersion = "v1.0.0"


}
```