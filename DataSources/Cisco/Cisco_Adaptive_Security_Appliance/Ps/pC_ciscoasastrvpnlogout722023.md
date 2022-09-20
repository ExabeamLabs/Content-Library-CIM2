#### Parser Content
```Java
{
Name = cisco-asa-str-vpn-logout-722023
  Vendor = Cisco
  Product = Cisco Adaptive Security Appliance
  ParserVersion = "v1.0.0"
  TimeFormat = "MMM dd yyyy HH:mm:ss"
  Conditions = [ 
  """-722023""" 
  """%ASA-""" 
  ]
  Fields = [
    """({time}\w+ \d+ \d{4} \d\d:\d\d:\d\d)"""
    """%ASA-({priority}\d+)-({event_code}\d+)"""
    """\sGroup\s*<({group_name}.*?)>"""
    """User <(({user_ou}\w+=[^<]+)|(({user}[^>@]+)(@({email_domain}[^>@]+))?))>"""
    """\sIP\s*<(({src_ip}(\d{1,3}\.){3}\d{1,3}|([A-Fa-f0-9%.]+:[A-Fa-f0-9%.:]+(th0)?))|({src_host}[^\s]+))>\s*({protocol}\w+)\s({event_name}SVC connection terminated)\s"""
  ]


}
```