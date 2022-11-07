#### Parser Content
```Java
{
Name = cisco-asa-kv-vpn-login-success-connected
Vendor = "Cisco"
Product = "Cisco Adaptive Security Appliance"
TimeFormat = "MM/dd/yyyy HH:mm:ss"
Conditions = [
  """ connected, Session Type:"""
  """AUTH/22"""
]
Fields = [
  """({time}\d+\/\d+\/\d+ \d+:\d+:\d+)"""
  """RPT=\d+\s+({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})"""
  """User\s+\[({user}[^\]]+)"""
]
ParserVersion = "v1.0.0"


}
```