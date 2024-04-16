#### Parser Content
```Java
{
Name = cisco-asa-str-network-notification-737006
  ParserVersion = v1.0.0
  Vendor = Cisco
  Product = Cisco Adaptive Security Appliance
  TimeFormat = ["MMM dd yyyy HH:mm:ss","yyyy-MM-dd'T'HH:mm:ss.SSSZ"]
  Conditions = [ """%ASA-""", """-737006""" ]
  Fields = [
    """({time}\d{4}\-\d{2}\-\d{2}T\d{2}:\d{2}:\d{2}\.\d+((\+|\-)\d\d:\d\d)?)\s+""",
    """\s(({host}[\w.\-]+))\s+([-\s:]+)?%ASA""",
    """%ASA-({priority}\d+)-({event_code}\d+)""",
    """({time}\w+ \d+ \d{4} \d\d:\d\d:\d\d).*?%ASA\-({priority}\d+)\-({event_code}\d+)""",
    """\sSession=({session_id}[^,]+)\s*""",
    """({event_name}Local pool request succeeded)""",
    """\stunnel-group '({group_name}[^']+)'""",
    """\w{3}\s+\d+\s+\d+\s+\d+:\d+:\d+\s+(\d+|({host}[\w\-\.]+))\s"""
  ]


}
```