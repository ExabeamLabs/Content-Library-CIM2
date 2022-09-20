#### Parser Content
```Java
{
Name = cisco-asa-kv-vpn-login-success-addressassigned
Vendor = "Cisco"
Product = "Cisco Adaptive Security Appliance"
TimeFormat = "epoch"
Conditions = [
  """Address assigned to session"""
  """|278-722051|"""
]
Fields = [
  """\srt=({time}\d+)"""
  """\sshost=({host}[^\s]+)"""
  """\ssuser=({user}.+?)\snitroGroup_Name ="""
  """\ssrc=({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})"""
  """\sdst=({src_translated_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})"""
]
ParserVersion = "v1.0.0"


}
```