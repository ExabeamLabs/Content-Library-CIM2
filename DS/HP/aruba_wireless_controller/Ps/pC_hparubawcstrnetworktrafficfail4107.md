#### Parser Content
```Java
{
Name = hp-arubawc-str-network-traffic-fail-4107
  ParserVersion = v1.0.0
  Vendor = HP
  Product = Aruba Wireless controller
  TimeFormat = "MMM dd HH:mm:ss yyyy"
  Conditions = [ """[4107]""", """ Dropping """, """Station""" ]
  Fields = [
    """({event_code}4107)""",
    """({event_name}Dropping.*?)\s*$""",
    """\d\d\d\d\s+({host}[^\s]+)\s""",
    """({time}\w+\s\d\d\s\d\d:\d\d:\d\d\s\d\d\d\d)""",
    """(for|by)\s(s|S)tation\s+({src_mac}[a-f0-9:]+)\s+({ssid}[a-f0-9:]+)""",
  ]


}
```