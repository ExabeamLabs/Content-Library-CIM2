#### Parser Content
```Java
{
Name = "cisco-asa-str-vpn-logout-722012"
  ParserVersion = "v1.0.0"
  Vendor = "Cisco"
  Product = "Cisco Adaptive Security Appliance"
  TimeFormat = "MMM dd yyyy HH:mm:ss"
  Conditions = [ """-722012""", """%ASA-""" ]
  Fields = [
    """%ASA-({priority}\d+)-({event_code}\d+)""",
    """\sGroup\s*<({group_name}[^\>]+)>""",
    """\sUser\s*<(({domain}[^\\>]+)\\)?(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-]{1,40}\$?))>""",
    """\sIP\s*<(({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})(:({src_port}\d+))?|([A-Fa-f0-9%.]*:[A-Fa-f0-9%.:]+(th0)?))|({src_host}[^\s]+?))>""",
    """({event_name}SVC Message)""",
    """Message:\s+({additional_info}[^@]+?)(\.|$)""",
    """({time}\w{3} \d+ \d{4} \d\d:\d\d:\d\d)\s*({host}[\w\-.]+)?\s*:\s*%ASA"""
    """\sGroup\s*<({group_name}[^>]+)>"""
    """\sUser\s*<({user}[\w\.\-]{1,40}\$?)>"""
  ]


}
```