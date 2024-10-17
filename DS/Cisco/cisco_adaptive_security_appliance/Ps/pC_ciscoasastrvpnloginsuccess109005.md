#### Parser Content
```Java
{
Name = cisco-asa-str-vpn-login-success-109005
Vendor = "Cisco"
Product = "Cisco Adaptive Security Appliance"
TimeFormat = "MMM dd yyyy HH:mm:ss"
Conditions = [
  """Authentication succeeded for user"""
  """-109005"""
]
Fields = [
  """({time}\w+ \d+ \d\d\d\d \d+:\d+:\d+)"""
  """Authentication succeeded for user '({user}[\w\.\-\!\#\^\~]{1,40}\$?)' from ({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}).+?to ({src_translated_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})"""
]
DupFields = [
  "user->account"
]
ParserVersion = "v1.0.0"


}
```