#### Parser Content
```Java
{
Name = cisco-asa-str-dns-response-fail-746016
  ParserVersion = v1.0.0
  Vendor = Cisco
  Product = Cisco Network Security
  TimeFormat = ["MMM dd yyyy HH:mm:ss", "MMM dd HH:mm:ss", "yyyy-MM-dd'T'HH:mm:ss.SSSZ"]
  Conditions = [ """-746016""", """%ASA-""" ]
  Fields = [
    """({time}\d{4}\-\d{2}\-\d{2}T\d{2}:\d{2}:\d{2}\.\d+((\+|\-)\d\d:\d\d)?)\s+""",
     """\s(({host}[\w.\-]+))\s+([-\s:]+)?%ASA""",
    """(({host}[\w\-.]+)\s+)?({time}\w+ \d\d (\d\d\d\d )?\d\d:\d\d:\d\d):\s*%ASA-({priority}\d+)""",
    """({time}\w+ \d\d (\d\d\d\d )?\d\d:\d\d:\d\d).*?%ASA-({priority}\d+)""",
    """({event_code}746016)""",
    """({event_name}DNS lookup) for ({dns_response}({dns_query}.+?)\sfailed)""",
    """,\s*reason\s*:\s*(UNKNOWN|({result_reason}.+?))\s*($|\w+=|'|")"""
    """\d\d:\d\d:\d\d\s+(::ffff:)?((?i)system|({host}[\w\.-]+))[\s:]+%ASA-"""
  ]
  DupFields = [ "result_reason->failure_reason" ]


}
```