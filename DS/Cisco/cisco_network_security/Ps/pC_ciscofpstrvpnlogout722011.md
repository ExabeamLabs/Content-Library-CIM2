#### Parser Content
```Java
{
Name = cisco-fp-str-vpn-logout-722011
  Vendor = Cisco
  Product = Cisco Network Security
  ParserVersion = "v1.0.0"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
  Conditions = [ """-722011""", """%FTD-""" ]
  Fields = [
    """({time}\d+-\d+-\d+T\d+:\d+:\d+Z)\s({host}[^\s]+)""",
    """\s(({host}[\w.\-]+))\s+([-\s:]+)?%FTD"""
    """%FTD-({priority}\d+)-({event_code}\d+)""",
    """Group\s*<({group_name}[^>]+)""",
    """User\s*<({user}[\w\.\-\!\#\^\~]{1,40}\$?)(?:@({domain}[^>]+))?>""",
    """IP <({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})>"""
    ]


}
```