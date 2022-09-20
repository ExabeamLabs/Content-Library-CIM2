#### Parser Content
```Java
{
Name = cisco-aci-str-endpoint-login-success-loginsession
Vendor = "Cisco"
Product = "ACI"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
  """ACI"""
  """login,session"""
  """Success"""
]
Fields = [
  """\d+:\d+:\d+(.\d+)?\s({host}[^\s]+)"""
  """remoteuser-({user}[^\]]+)"""
  """From-({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})"""
  """({result}Success)"""
]
ParserVersion = "v1.0.0"


}
```