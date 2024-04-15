#### Parser Content
```Java
{
Name = "vmware-horizon-str-endpoint-login-success-startingchannel"
Vendor = "VMware"
Product = "VMware Horizon"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
Conditions = [
  """starting channel """
  """connecting to target"""
]
Fields = [
  """connecting to target (?:({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})|({dest_host}[^\s:]+))"""
  """User ({user}.+?) starting channel"""
]
ParserVersion = "v1.0.0"


}
```