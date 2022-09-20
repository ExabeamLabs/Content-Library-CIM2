#### Parser Content
```Java
{
Name = cisco-asa-str-vpn-login-722033
  Vendor = Cisco
  Product = Cisco Adaptive Security Appliance
  ParserVersion = "v1.0.0"
  TimeFormat = "MMM dd yyyy HH:mm:ss"
  Conditions = [ 
  """-722033"""
  """%ASA-""" 
  ]
  Fields = [
    """({time}\w+ \d+ \d{4} \d\d:\d\d:\d\d)"""
    """%ASA-({priority}\d+)-({event_code}\d+)"""
    """\sGroup\s*<({group_name}[^>]+)>"""
    """\sUser\s*<(({email_address}[^@]+@[^>]+)|(({domain}[^\\>]+)\\+)?({user}[^>]+))>""",
    """\sIP\s*<(({src_ip}(\d{1,3}\.){3}\d{1,3}|([^:]+?:[A-Fa-f0-9%.:]+(th0)?))|({src_host}[^\s]+))>"""
    """({event_name}First\s*(TCP|UDP|)\s*SVC connection established for SVC session)"""
    """({protocol}SVC)"""
  ]


}
```