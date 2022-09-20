#### Parser Content
```Java
{
Name = cisco-fp-str-network-notification-722036
  Vendor = Cisco
  Product = Cisco Firepower
  ParserVersion = "v1.0.0"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
  Conditions = [ """-722036""", """%FTD-""" ]
  Fields = [
    """({time}\d+-\d+-\d+T\d+:\d+:\d+Z)\s({host}[^\s]+)""",
    """%FTD-({priority}\d+)-({event_code}\d+)""",
    """({event_name}Transmitting large packet)""",
    """IP\s*<(({src_ip}(\d{1,3}\.){3}\d{1,3}|([A-Fa-f0-9%.]*:[A-Fa-f0-9%.:]+(th0)?))|({src_host}[^\s]+?))""",
    """Group\s*<({group_name}[^>]+)""",
    """User\s*<(({email_domain}[^\\]+)\\+)?({user}[^>\\]+)"""
    """User\s*<({user}[^@>\\]+)(?:@({email_domain}[^>]+))?>""",
    ]


}
```