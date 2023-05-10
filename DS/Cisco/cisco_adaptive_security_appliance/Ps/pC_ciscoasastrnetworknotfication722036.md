#### Parser Content
```Java
{
Name = cisco-asa-str-network-notfication-722036
  Vendor = Cisco
  Product = Cisco Adaptive Security Appliance
  ParserVersion = "v1.0.0"
  TimeFormat = "MMM dd yyyy HH:mm:ss"
  Conditions = [ """-722036""", """%ASA-""" ]
  Fields = [
    """({time}\w+ \d\d \d\d\d\d \d\d:\d\d:\d\d)""",
    """:\s*%ASA-({priority}\d+)""",
    """({event_code}722036)""",
    """({event_name}Transmitting large packet)""",
    """IP\s*<(({src_ip}(\d{1,3}\.){3}\d{1,3}|([A-Fa-f0-9%.]*:[A-Fa-f0-9%.:]+(th0)?))|({src_host}[^\s]+?))""",
    """Group\s*<({group_name}[^>]+)""",
    """User\s*<(({domain}[^\\]+)\\+)?({user}[^>\\]+)"""
    """User\s*<({user}[^@>\\]+)(?:@({domain}[^>]+))?>""",
  ]


}
```