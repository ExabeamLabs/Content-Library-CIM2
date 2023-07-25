#### Parser Content
```Java
{
Name = cisco-asa-kv-vpn-logout-611103
  Vendor = Cisco
  Product = Cisco Adaptive Security Appliance
  ParserVersion = "v1.0.0"
  TimeFormat = "MMM dd yyyy HH:mm:ss"
  Conditions = [ 
  """%ASA-"""
  """-611103""" 
  ]
  Fields = [
    """({time}\w+ \d+ \d{4} \d\d:\d\d:\d\d)\s*(({host}[\w.\-]+))?\s*:\s*%ASA\-({priority}\d+)\-({event_code}\d+)"""
    """-611103:\s*({event_name}User logged out)"""
    """Uname:\s*({user}\w+)"""
  ]


}
```