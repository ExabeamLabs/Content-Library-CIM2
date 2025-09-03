#### Parser Content
```Java
{
Name = "cisco-asa-str-app-notification-302010"
  Vendor = "Cisco"
  Product = Cisco Network Security
  TimeFormat = ["MMM dd yyyy HH:mm:ss", "yyyy-MM-dd'T'HH:mm:ss.SSSZ"]
  ParserVersion = "v1.0.0"
  Conditions = [ """-302010""", """%ASA-""" ]
  Fields = [
    """({time}\d{4}\-\d{2}\-\d{2}T\d{2}:\d{2}:\d{2}\.\d+((\+|\-)\d\d:\d\d)?)\s+""",
"""\s(({host}[\w.\-]+))\s+([-\s:]+)?%ASA""",
    """({time}\w+ \d+ \d{4} \d\d:\d\d:\d\d)""",
    """%ASA-({priority}\d+)-({event_code}\d+)""",
    """\s(::ffff:)?(-|({host}[\w\.-]+))[\s:]+%ASA-"""
  ]


}
```