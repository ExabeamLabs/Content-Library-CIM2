#### Parser Content
```Java
{
Name = "cisco-asa-kv-vpn-logout-success-113019"
Vendor = "Cisco"
Product = "Cisco Adaptive Security Appliance"
TimeFormat = "epoch"
Conditions = [
  """Session disconnected"""
  """|278-113019|"""
]
Fields = [
  """\srt=({time}\d{13})"""
  """\sshost=({host}[^\s]+)"""
  """\ssuser=({user}[\w\.\-]{1,40}\$?)\s+"""
  """\ssrc=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
]
ParserVersion = "v1.0.0"


}
```