#### Parser Content
```Java
{
Name = cisco-asa-str-network-traffic-fail-313005
  ParserVersion = v1.0.0
  Vendor = Cisco
  Product = Cisco Adaptive Security Appliance
  TimeFormat = "MMM dd yyyy HH:mm:ss"
  Conditions = [ """-313005""", """%ASA-""", """error message:""" ]
  Fields = [
    """\w+ \d+ \d{4} \d\d:\d\d:\d\d (::ffff:)?({host}\S+) : %ASA""",
    """({time}\w+ \d+ \d{4} \d\d:\d\d:\d\d)""",
    """%ASA-({priority}\d+)-({event_code}\d+):\s*({event_name}.*?)\sfor\s*({protocol}\w+)\s""",
    """\ssrc\s*({src_interface}\w+):((::ffff:)?({src_ip}(\d{1,3}\.){3}\d{1,3}|([A-Fa-f0-9%.]*:[A-Fa-f0-9%.:]+(th0)?))|(::ffff:)?({src_host}[^\s]+?))(\(({domain}[^\\]+)\\({email_address}[^@]+@[^.]+\.[^)]+)|({user}[^\\]+?)\))?""",
    """\sdst\s*({dest_interface}\w+):((::ffff:)?({dest_ip}(\d{1,3}\.){3}\d{1,3}|([A-Fa-f0-9%.]*:[A-Fa-f0-9%.:]+(th0)?))|(::ffff:)?({dest_host}[^\s]+?)(\s|$))""",
  ]


}
```