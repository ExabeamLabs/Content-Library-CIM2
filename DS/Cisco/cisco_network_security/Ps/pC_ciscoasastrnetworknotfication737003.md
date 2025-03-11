#### Parser Content
```Java
{
Name = cisco-asa-str-network-notfication-737003
  Vendor = Cisco
  Product = Cisco Network Security
  ParserVersion = v1.0.0
  TimeFormat = ["MMM dd yyyy HH:mm:ss","yyyy-MM-dd'T'HH:mm:ss.SSSZ"]
  Conditions = [ """%ASA-""", """-737003""" ]
  Fields = [
    """({time}\d{4}\-\d{2}\-\d{2}T\d{2}:\d{2}:\d{2}\.\d+((\+|\-)\d\d:\d\d)?)\s+""",
    """\s(({host}[\w.\-]+))\s+([-\s:]+)?%ASA""",
    """%ASA-({priority}\d+)-({event_code}\d+)""",
    """({time}\w+ \d+ \d{4} \d\d:\d\d:\d\d)\s*({host}[\w\.-]+)?\s*:\s*%ASA\-({priority}\d+)\-({event_code}\d+)""",
    """:\s+Session=({session_id}[^\s,]+)""",
    """({event_name}DHCP configured, no viable servers found)""",
  ]


}
```