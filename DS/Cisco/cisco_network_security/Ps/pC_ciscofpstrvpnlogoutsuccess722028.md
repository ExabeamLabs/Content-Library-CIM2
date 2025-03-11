#### Parser Content
```Java
{
Name = "cisco-fp-str-vpn-logout-success-722028"
  ParserVersion = "v1.0.0"
  Vendor = "Cisco"
  Product = Cisco Network Security
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
  Conditions = [ """-722028""", """%FTD-""" ]
  Fields = [
    """({time}\d+-\d+-\d+T\d+:\d+:\d+Z)\s({host}[^\s]+)""",
    """\s(({host}[\w.\-]+))\s+([-\s:]+)?%FTD"""
    """%FTD-({priority}\d+)-({event_code}\d+)""",
    """Group\s*<({group_name}[^>]+)""",
    """User\s*<({user}[\w\.\-\!\#\^\~]{1,40}\$?)(?:@({domain}[^>]+))?>""",
  ]


}
```