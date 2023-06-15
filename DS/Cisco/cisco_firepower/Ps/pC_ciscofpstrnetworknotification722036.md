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
    """IP\s*<(({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})(:({src_port}\d+))?|([A-Fa-f0-9%.]*:[A-Fa-f0-9%.:]+(th0)?))|({src_host}[^\s]+?))""",
    """Group\s*<({group_name}[^>]+)""",
    """User\s*<(({domain}[^\\]+)\\+)?({user}[^>\\]+)"""
    """User\s*<({user}[^@>\\]+)(?:@({domain}[^>]+))?>""",
    ]


}
```