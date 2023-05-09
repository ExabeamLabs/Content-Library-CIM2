#### Parser Content
```Java
{
Name = cisco-asa-str-dns-response-fail-746016
  ParserVersion = v1.0.0
  Vendor = Cisco
  Product = Cisco Adaptive Security Appliance
  TimeFormat = "MMM dd yyyy HH:mm:ss"
  Conditions = [ """-746016""", """%ASA-""" ]
  Fields = [
    """({host}[\w\-.]+)\s+({time}\w+ \d\d \d\d\d\d \d\d:\d\d:\d\d):\s*%ASA-({priority}\d+)""",
    """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d(\+|\-)\d\d:\d\d)\s+({host}\S+)\s+:\s*%ASA-({priority}\d+)""",
    """({event_code}746016)""",
    """({event_name}DNS lookup) for ({dns_response}({dns_query}.+?)\s({dns_response_code}failed))""",
    """,\s*reason\s*:\s*(UNKNOWN|({result_reason}.+?))\s*($|\w+=|'|")"""
  ]


}
```