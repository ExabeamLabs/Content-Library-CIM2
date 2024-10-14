#### Parser Content
```Java
{
Name = "f5-bigipapm-str-vpn-login-success-username"
Vendor = "F5"
Product = "F5 Access Policy Manager"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
  """01490143:5:"""
  """username:"""
]
Fields = [
  """:Common:({session_id}[^:]+)"""
  """\s+01490143:5:.*?({session_id}[^\s:]+): Logging Agent"""
  """\susername:\s+({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""
  """ip_address:\s*({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))"""
]
ParserVersion = "v1.0.0"


}
```