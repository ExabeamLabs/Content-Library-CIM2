#### Parser Content
```Java
{
Name = cisco-asa-str-user-permission-modify-502103
  Vendor = Cisco
  Product = Cisco Adaptive Security Appliance
  ParserVersion = "v1.0.0"
  TimeFormat = "MMM dd yyyy HH:mm:ss"
  Conditions = [ 
  """%ASA-"""
  """-502103""" 
  ]
  Fields = [
    """({time}\w+ \d+ \d{4} \d\d:\d\d:\d\d):\s*%ASA\-({priority}\d+)\-({event_code}\d+)"""
    """-502103:\s*({event_name}User priv level changed)"""
    """Uname:\s+({user}.+?)\s+From"""
# info is removed
]


}
```