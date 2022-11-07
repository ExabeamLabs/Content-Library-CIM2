#### Parser Content
```Java
{
Name = cisco-asa-str-vpn-login-722032
  Vendor = Cisco
  Product = Cisco Adaptive Security Appliance
  ParserVersion = "v1.0.0"
  TimeFormat = "MMM dd yyyy HH:mm:ss"
  Conditions = [ 
  """-722032"""
  """%ASA-""" 
  ]
  Fields = [
    """(Original Address=({host}\S+) )?({time}\w+ \d+ \d\d\d\d \d\d:\d\d:\d\d)( ({=host}[\w\-.]+))?"""
    """%ASA-({priority}\d+)-({event_code}\d+)"""
    """\sGroup\s*<({group_name}.+?)>"""
    """\sUser\s*<({user}[^@>]+)(?:@({email_domain}[^>]+))?>"""
    """\sIP\s*<(({src_ip}(\d{1,3}\.){3}\d{1,3}|([A-Fa-f0-9%.]*:[A-Fa-f0-9%.:]+(th0)?))|({src_host}[^\s]+))>"""
    """({event_name}New\s({protocol}\w+)\s+SVC connection)"""
  ]


}
```