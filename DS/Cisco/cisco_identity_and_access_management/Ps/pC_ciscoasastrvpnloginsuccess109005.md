#### Parser Content
```Java
{
Name = cisco-asa-str-vpn-login-success-109005
Vendor = "Cisco"
Product = "Cisco Identity and Access Management"
TimeFormat = "MMM dd yyyy HH:mm:ss"
Conditions = [
  """Authentication succeeded for user"""
  """-109005"""
  """%ASA-"""
]
Fields = [
  """({time}\w+ \d+ \d\d\d\d \d+:\d+:\d+)"""
  """Authentication succeeded for user '({account}({user}[\w\.\-\!\#\^\~]{1,40}\$?))' from ({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}).+?to ({src_translated_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})"""
]
ParserVersion = "v1.0.0"


}
```