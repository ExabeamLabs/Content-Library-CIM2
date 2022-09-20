#### Parser Content
```Java
{
Name = hp-arubawc-str-network-traffic-4111
  ParserVersion = v1.0.0
  Vendor = HP
  Product = Aruba Wireless controller
  TimeFormat = "MMM dd HH:mm:ss yyyy"
  Conditions = [ """[4111]""", """ Assoc """ ]
  Fields = [
    """({event_name}Assoc.*?)\s*$""",
    """({event_code}4111)""",
    """\d\d\d\d\s+({host}[^\s]+)\s""",
    """({time}\w+\s\d\d\s\d\d:\d\d:\d\d\s\d\d\d\d)""",
    """({src_mac}[a-f0-9:]+):\s({action}\w+)\s""",
  ]


}
```