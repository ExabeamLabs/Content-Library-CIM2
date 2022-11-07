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
  """\srt=({time}\d+)"""
  """\sdst=({dest_ip}[a-fA-F\d.:]+)"""
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