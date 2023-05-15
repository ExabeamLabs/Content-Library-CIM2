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
    """from\s*(({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})(:({src_port}\d+))?|([A-Fa-f0-9%.]*:[A-Fa-f0-9%.:]+(th0)?))|({src_host}[^\s]+?))""",
    """interface\s*({interface}[^\s]+)\s*for""",
    """user\s*"(Unknown|({user}[^"\*\s]+))"""
  ]


}
```