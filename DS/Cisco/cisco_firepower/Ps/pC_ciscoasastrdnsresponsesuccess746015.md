#### Parser Content
```Java
{
Name = cisco-asa-str-dns-response-success-746015
  ParserVersion = v1.0.0
  Vendor = Cisco
  Product = Cisco Firepower
  TimeFormat = "MMM dd yyyy HH:mm:ss"
  Conditions = [ """%FTD-""", """-746015""", """ resolved""" ]
  Fields = [
    """({time}\w+\s\d\d\s\d\d\d\d\s\d\d:\d\d:\d\d)\s({host}[\w\-.]+)\s:\s*%FTD-""",
    """%FTD-({priority}\d)-({event_code}[^:]+)""",
    """\]\s({dns_response}({query}\S+)\s({dns_response_code}resolved)[^=]+?)\s*$"""
]


}
```