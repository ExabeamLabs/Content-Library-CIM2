#### Parser Content
```Java
{
Name = cisco-asa-cef-vpn-login-success-assignedprivateip
Vendor = "Cisco"
Product = "Cisco Adaptive Security Appliance"
TimeFormat = "epoch"
Conditions = [
  """CEF:"""
  """|CISCO|ASA|"""
  """|Assigned private IP address|"""
  """sourceTranslatedAddress"""
]
Fields = [
  """\srt=({time}\d*)"""
  """\ssourceTranslatedAddress=({src_translated_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})"""
  """\ssuser=({user}.+?)\s+(\w+=|$)"""
  """\ssrc=({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})"""
  """\sdvc=({host}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})"""
  """\sdvchost=({host}.+?)\s+(\w+=|$)"""
]
ParserVersion = "v1.0.0"


}
```