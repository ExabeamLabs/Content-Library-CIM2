#### Parser Content
```Java
{
Name = cisco-asa-str-ip-assign-fail-737034
  ParserVersion = v1.0.0
  Vendor = Cisco
  Product = Cisco Adaptive Security Appliance
  TimeFormat = "MMM dd yyyy HH:mm:ss"
  Conditions = [ """%ASA-""", """-737034""" ]
  Fields = [
    """({time}\w+ \d+ \d{4} \d\d:\d\d:\d\d):\s*%ASA\-({priority}\d+)\-({event_code}\d+)""",
    """\sSession=({session_id}[^,]+)\s*""",
    """IPv(4|6) address:\s*({event_name}[^,]+?)\s*("*,|$)"""
  ]
  DupFields = [ "event_name->failure_reason" ]


}
```