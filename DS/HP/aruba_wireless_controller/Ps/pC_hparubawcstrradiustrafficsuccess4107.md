#### Parser Content
```Java
{
Name = hp-arubawc-str-radius-traffic-success-4107
  ParserVersion = v1.0.0
  Vendor = HP
  Product = Aruba Wireless controller
  TimeFormat = "MMM dd HH:mm:ss yyyy"
  Conditions = [ """[4107]""", """ RADIUS """ ]
  Fields = [
    """({event_code}4107)""",
    """({event_name}RADIUS.*?)\s*$""",
    """\d\d\d\d\s+({host}[^\s]+)\s""",
    """({time}\w+\s\d\d\s\d\d:\d\d:\d\d\s\d\d\d\d)""",
    """\s+({ssid}[a-f0-9:]+)\sfrom\sserver""",
    """4107\][^"]+\s({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})>"""
  ]


}
```