#### Parser Content
```Java
{
Name = cisco-asa-str-ip-assign-fail-737034
  ParserVersion = v1.0.0
  Vendor = Cisco
  Product = Cisco Network Security
  TimeFormat = ["MMM dd yyyy HH:mm:ss","yyyy-MM-dd'T'HH:mm:ss.SSSZ"]
  Conditions = [ """%ASA-""", """-737034""" ]
  Fields = [
    """({time}\d{4}\-\d{2}\-\d{2}T\d{2}:\d{2}:\d{2}\.\d+((\+|\-)\d\d:\d\d)?)\s+""",
    """\s(({host}[\w.\-]+))\s+([-\s:]+)?%ASA""",
    """%ASA-({priority}\d+)-({event_code}\d+)""",
    """({time}\w+ \d+ \d{4} \d\d:\d\d:\d\d).*?%ASA\-({priority}\d+)\-({event_code}\d+)""",
    """\sSession=({session_id}[^,]+)\s*""",
    """IPv(4|6) address:\s*({event_name}[^,]+?)\s*("*,|$)""",
    """\s(::ffff:)?(-|({host}[\w\.-]+))[\s:]+%ASA-"""
    """IPv(4|6) address:\s*({failure_reason}[^,]+?)\s*("*,|$)""",
  ]


}
```