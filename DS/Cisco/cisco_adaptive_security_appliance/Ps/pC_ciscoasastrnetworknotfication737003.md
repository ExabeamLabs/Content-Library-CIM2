#### Parser Content
```Java
{
Name = cisco-asa-str-network-notfication-737003
  Vendor = Cisco
  Product = Cisco Adaptive Security Appliance
  ParserVersion = v1.0.0
  TimeFormat = "MMM dd yyyy HH:mm:ss"
  Conditions = [ """%ASA-""", """-737003""" ]
  Fields = [
    """({time}\w+ \d+ \d{4} \d\d:\d\d:\d\d):\s*%ASA\-({priority}\d+)\-({event_code}\d+)""",
    """:\s+Session=({session_id}[^\s,]+)""",
    """({event_name}DHCP configured, no viable servers found)""",
  ]


}
```