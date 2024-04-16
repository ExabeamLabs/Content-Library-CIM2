#### Parser Content
```Java
{
Name = cisco-asa-str-user-modify-fail-746010
  Vendor = Cisco
  Product = Cisco Adaptive Security Appliance
  ParserVersion = v1.0.0
  TimeFormat = "MMM dd yyyy HH:mm:ss"
  Conditions = [ """-746010""", """%ASA-""" ]
  Fields = [
    """({host}[\w\-.]+)\s+({time}\w+ \d\d (\d\d\d\d )?\d\d:\d\d:\d\d):\s*%ASA-({priority}\d+)""",
    """({event_code}746010)""",
    """({event_name}Update import-user) ({domain}\S+) ({group_name}\S+)""",
    """ - Import Failed - ({result_reason}.+?)\s*$"""
  ]


}
```