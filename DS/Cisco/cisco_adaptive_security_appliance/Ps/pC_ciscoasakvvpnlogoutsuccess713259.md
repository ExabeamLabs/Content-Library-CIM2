#### Parser Content
```Java
{
Name = "cisco-asa-kv-vpn-logout-success-713259"
Vendor = "Cisco"
Product = "Cisco Adaptive Security Appliance"
TimeFormat = "epoch"
Conditions = [
  """Session is being torn down"""
  """|278-713259|"""
]
Fields = [
  """\srt=({time}\d{13})"""
  """\sshost=({host}[^\s]+)"""
  """\ssrc=({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  """\ssuser=({user}[^\r\n]+)\s+"""
]
ParserVersion = "v1.0.0"


}
```