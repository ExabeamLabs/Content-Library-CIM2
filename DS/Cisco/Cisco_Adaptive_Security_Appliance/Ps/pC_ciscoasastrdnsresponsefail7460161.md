#### Parser Content
```Java
{
Name = cisco-asa-str-dns-response-fail-746016-1
  ParserVersion = v1.0.0
  Vendor = Cisco
  Product = Cisco Adaptive Security Appliance
  TimeFormat = "MMM dd yyyy HH:mm:ss"
  Conditions = [ """%FTD-""", """-746016""" ]
  Fields = [
    """\d\d:\d\d:\d\d\s({host}[\w\-.]+)\s""",
    """({time}\w+\s\d\d\s\d\d\d\d\s\d\d:\d\d:\d\d)\s({host}[\w\-.]+)\s:\s*%FTD-""",
    """%FTD-({priority}\d)-({event_code}[^:]+)""",
    """({event_name}DNS lookup) for ({dns_response}({query}\S+)\s({dns_response_code}failed))""",
    """,\s*reason\s*:\s*(UNKNOWN|({failure_reason}[^=]+?))\s*($|\")"""
]


}
```