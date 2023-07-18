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
    """Uname:\s+(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\-\.]{1,40}))\s+From"""
# info is removed
]


}
```