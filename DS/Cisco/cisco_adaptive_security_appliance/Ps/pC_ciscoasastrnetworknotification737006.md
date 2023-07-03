#### Parser Content
```Java
{
Name = cisco-asa-str-network-notification-737006
  ParserVersion = v1.0.0
  Vendor = Cisco
  Product = Cisco Adaptive Security Appliance
  TimeFormat = "MMM dd yyyy HH:mm:ss"
  Conditions = [ """%ASA-""", """-737006""" ]
  Fields = [
    """({time}\w+ \d+ \d{4} \d\d:\d\d:\d\d).*?%ASA\-({priority}\d+)\-({event_code}\d+)""",
    """\sSession=({session_id}[^,]+)\s*""",
    """({event_name}Local pool request succeeded)""",
    """\stunnel-group '({group_name}[^']+)'"""
  ]


}
```