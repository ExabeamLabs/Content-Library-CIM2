#### Parser Content
```Java
{
Name = hp-arubawc-str-app-notification-success-4107-1
  ParserVersion = v1.0.0
  Vendor = HP
  Product = Aruba Wireless controller
  TimeFormat = "MMM dd HH:mm:ss yyyy"
  Conditions = [ """[4107]""", """ WPA2 """ ]
  Fields = [
    """({event_code}4107)""",
    """({event_name}WPA2.*?)\s*$""",
    """\d\d\d\d\s+({host}[^\s]+)\s""",
    """({time}\w+\s\d\d\s\d\d:\d\d:\d\d\s\d\d\d\d)""",
  ]


}
```