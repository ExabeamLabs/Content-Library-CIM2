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
    """IP\s*<(({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})(:({src_port}\d+))?|([A-Fa-f0-9%.]*:[A-Fa-f0-9%.:]+(th0)?))|({src_host}[^\s]+?))""",
    """Group\s*<({group_name}[^>]+)""",
    """User\s*<(({domain}[^\\]+)\\+)?({user}[^>\\]+)"""
    """User\s*<({user}[^@>\\]+)(?:@({domain}[^>]+))?>""",
  ]


}
```