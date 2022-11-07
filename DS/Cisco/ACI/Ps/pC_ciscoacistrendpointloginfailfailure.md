#### Parser Content
```Java
{
Name = cisco-aci-str-endpoint-login-fail-failure
Vendor = "Cisco"
Product = "ACI"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
  """ACI"""
  """login,session"""
  """Failure"""
]
Fields = [
  """\d+:\d+:\d+(.\d+)?\s({host}[^\s]+)"""
  """From-({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})"""
  """({result}Failure)"""
]
ParserVersion = "v1.0.0"


}
```