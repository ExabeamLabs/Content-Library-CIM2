#### Parser Content
```Java
{
Name = cisco-aci-str-endpoint-login-fail-failure
Vendor = "Cisco"
Product = "Cisco Data Center"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
  """ACI"""
  """login,session"""
  """Failure"""
]
Fields = [
  """\d+:\d+:\d+(.\d+)?\s({host}[^\s]+)"""
  """From-({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  """({result}Failure)"""
]
ParserVersion = "v1.0.0"


}
```