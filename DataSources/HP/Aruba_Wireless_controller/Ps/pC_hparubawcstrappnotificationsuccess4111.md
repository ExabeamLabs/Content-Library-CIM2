#### Parser Content
```Java
{
Name = hp-arubawc-str-app-notification-success-4111
  ParserVersion = v1.0.0
  Vendor = HP
  Product = Aruba Wireless controller
  TimeFormat = "MMM dd HH:mm:ss yyyy"
  Conditions = [ """[4111]""", """ AP """, """ protection """ ]
  Fields = [
    """({event_code}4111)""",
    """({event_name}AP.*?)\s*$""",
    """\d\d\d\d\s+({host}[^\s]+)\s""",
    """({time}\w+\s\d\d\s\d\d:\d\d:\d\d\s\d\d\d\d)""",
  ]


}
```