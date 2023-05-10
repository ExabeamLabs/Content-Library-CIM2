#### Parser Content
```Java
{
Name = cisco-asa-str-app-authentication-722055
  ParserVersion = v1.0.0
  Vendor = Cisco
  Product = Cisco Adaptive Security Appliance
  TimeFormat = "MMM dd yyyy HH:mm:ss"
  Conditions = [ """%ASA-""", """-722055""" ]
  Fields = [
    """({time}\w+ \d+ \d{4} \d\d:\d\d:\d\d)""",
    """%ASA\-({priority}\d+)\-({event_code}\d+)""",
    """Group <({group_name}[^>]+)>""",
    """\sUser\s*<(({domain}[^\\>]+)\\)?(({email_address}[^\@]+\@[^>]+)|({user}[^>]+))>""",
    """IP <(({src_ip}(\d{1,3}\.){3}\d{1,3}|([A-Fa-f0-9%.]*:[A-Fa-f0-9%.:]+(th0)?))|({src_host}[^\s]+?))""",
    """({event_name}AnyConnect VPN Agent)"""
  ]
  DupFields = [ "group_name->realm" ]


}
```