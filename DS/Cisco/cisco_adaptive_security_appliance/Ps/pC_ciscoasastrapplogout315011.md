#### Parser Content
```Java
{
Name = cisco-asa-str-app-logout-315011
  ParserVersion = v1.0.0
  Vendor = Cisco
  Product = Cisco Adaptive Security Appliance
  TimeFormat = "MMM dd yyyy HH:mm:ss"
  Conditions = [ """-315011""", """%ASA-""" ]
  Fields = [
    """({time}\w+ \d\d \d\d\d\d \d\d:\d\d:\d\d):\s*%ASA-({priority}\d+)""",
    """({event_code}315011)""",
    """({event_name}disconnected by SSH server)""",
# trust_point is removed
    """from\s*(({src_ip}(\d{1,3}\.){3}\d{1,3}|([A-Fa-f0-9%.]*:[A-Fa-f0-9%.:]+(th0)?))|({src_host}[^\s]+?))""",
    """interface\s*({interface}[^\s]+)\s*for""",
    """user\s*"(Unknown|({user}[^"\*\s]+))"""
  ]


}
```