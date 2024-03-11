#### Parser Content
```Java
{
Name = cisco-asa-cef-vpn-login-success-721016
Vendor = "Cisco"
Product = "Cisco Adaptive Security Appliance"
TimeFormat = "epoch"
Conditions = [
  """|CISCO|ASA|"""
  """|721016|"""
  """|WebVPN session created|"""
]
Fields = [
  """\srt=({time}\d{13})"""
  """\sdst=({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
  """\sduser=({user}.+?)\s+(\w+=|$)"""
  """\sdvchost=({host}.+?)\s+(\w+=|$)"""
  """\sdhost=({dest_host}.+?)\s+\w+="""
]
DupFields = [
  "user->account"
]
ParserVersion = "v1.0.0"


}
```