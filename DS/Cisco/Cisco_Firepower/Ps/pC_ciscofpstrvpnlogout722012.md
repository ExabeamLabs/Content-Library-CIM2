#### Parser Content
```Java
{
Name = cisco-fp-str-vpn-logout-722012
  Vendor = Cisco
  Product = Cisco Firepower
  ParserVersion = "v1.0.0"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
  Conditions = [ """-722012""", """%FTD-""" ]
  Fields = [
    """({time}\d+-\d+-\d+T\d+:\d+:\d+Z)\s({host}[^\s]+)""",
    """%FTD-({priority}\d+)-({event_code}\d+)""",
    """\sGroup\s*<({group_name}.*?)>""",
    """\sUser\s*<({user}[^@>]+)(?:@({email_domain}[^>]+))?>""",
    """\sIP\s*<(({src_ip}(\d{1,3}\.){3}\d{1,3}|([A-Fa-f0-9%.]*:[A-Fa-f0-9%.:]+(th0)?))|({src_host}[^\s]+?))>\s.*:\s({event_name}[\w\s]+)(\.|$)"""
  ]


}
```