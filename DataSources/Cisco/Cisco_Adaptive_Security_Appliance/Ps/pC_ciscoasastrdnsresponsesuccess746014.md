#### Parser Content
```Java
{
Name = cisco-asa-str-dns-response-success-746014
  ParserVersion = v1.0.0
  Vendor = Cisco
  Product = Cisco Adaptive Security Appliance
  TimeFormat = "MMM dd yyyy HH:mm:ss"
  Conditions = [ """%FTD-""", """-746014""", """ address """, """ obsolete""" ]
  Fields = [
    """({time}\w+\s\d\d\s\d\d\d\d\s\d\d:\d\d:\d\d)\s({host}[\w\-.]+)\s:\s*%FTD-""",
    """%FTD-({priority}\d)-({event_code}[^:]+)""",
    """\]\s({dns_response}({query}\S+)[^=]+?({dns_response_code}obsolete))""",
]


}
```