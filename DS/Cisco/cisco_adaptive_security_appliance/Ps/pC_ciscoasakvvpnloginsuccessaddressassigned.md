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
  """\srt=({time}\d{13})"""
  """\sshost=({host}[^\s]+)"""
  """\ssuser=({user}[\w\.\-]{1,40}\$?)\snitroGroup_Name ="""
  """\ssrc=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  """\sdst=({src_translated_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})"""
]
ParserVersion = "v1.0.0"


}
```