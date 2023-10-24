#### Parser Content
```Java
{
Name = "juniper-srx-kv-endpoint-login-success-uiloginevent"
Vendor = "Juniper Networks"
Product = "Juniper SRX Series"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
Conditions = [
  """UI_LOGIN_EVENT"""
]
Fields = [
  """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)(?:z|Z)?"""
  """\s({host}[^\s]*)\s(\w+|-)\s(\d+|-)\sUI_LOGIN_EVENT"""
  """username=\"(?!N\/A)({user}[\w\.\-]{1,40}\$?)\"\s"""
  """ssh-connection=\"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))\s({src_port}\d+)\s({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))\s({dest_port}\d+)\"\s"""
  """({event_name}UI_LOGIN_EVENT)"""
]
ParserVersion = "v1.0.0"


}
```