#### Parser Content
```Java
{
Name = cisco-asa-str-ip-assign-fail-722041
  ParserVersion = v1.0.0
  Vendor = Cisco
  Product = Cisco Adaptive Security Appliance
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """%ASA-""", """-722041""", """TunnelGroup """ ]
  Fields = [
    """\s.*?({host}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})\s+%ASA-""",
    """%ASA-({priority}\d+)-({event_code}\d+)""",
    """\sUser\s+<(({domain}[^\\]+)\\)?({user}[^>]+)>""",
    """\sIP\s+<({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})>""",
    """ Group\s+<({realm}.+?)>""",
    """({time}\w+ \d+ \d{4} \d\d:\d\d:\d\d).*?%ASA-"""
  ]


}
```