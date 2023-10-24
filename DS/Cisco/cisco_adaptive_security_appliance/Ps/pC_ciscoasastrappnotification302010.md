#### Parser Content
```Java
{
Name = "cisco-asa-str-app-notification-302010"
  Vendor = "Cisco"
  Product = "Cisco Adaptive Security Appliance"
  TimeFormat = "MMM dd yyyy HH:mm:ss"
  ParserVersion = "v1.0.0"
  Conditions = [ """-302010""", """%ASA-""" ]
  Fields = [
    """({time}\w+ \d+ \d{4} \d\d:\d\d:\d\d)""",
    """%ASA-({priority}\d+)-({event_code}\d+)"""
  ]


}
```