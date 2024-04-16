#### Parser Content
```Java
{
Name = cisco-asa-str-network-session-fail-752012
  ParserVersion = v1.0.0
  Vendor = Cisco
  Product = Cisco Adaptive Security Appliance
  TimeFormat = "MMM dd yyyy HH:mm:ss"
  Conditions = [ """-752012""", """%ASA-""" ]
  Fields = [
    """(::ffff:)?(({host}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})\s*)?({time}\w+ \d+ \d{4} \d\d:\d\d:\d\d)""",
    """%ASA\-({priority}\d+)\-({event_code}\d+)""",
    """({failure_reason}({protocol}\w+) was ({event_name}unsuccessful at setting up a tunnel))""",
    """\w{3}\s+\d+\s+\d+\s+\d+:\d+:\d+\s+(\d+|({host}[\w\-\.]+))\s"""
  ]


}
```