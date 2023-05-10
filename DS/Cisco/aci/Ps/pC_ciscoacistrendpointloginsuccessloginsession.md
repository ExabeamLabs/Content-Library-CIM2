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
  """From-({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  """({result}Success)"""
]
ParserVersion = "v1.0.0"


}
```