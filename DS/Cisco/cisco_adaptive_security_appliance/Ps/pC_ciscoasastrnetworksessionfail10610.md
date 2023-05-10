#### Parser Content
```Java
{
Name = cisco-asa-str-network-session-fail-10610
  ParserVersion = v1.0.0
  Vendor = Cisco
  Product = Cisco Adaptive Security Appliance
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """%ASA-""", """-10610""", """: access-list """, """hit-cnt""" ]
  Fields = [
    """({time}\w+ \d\d \d\d\d\d \d\d:\d\d:\d\d+)""",
    """(\w{3} (\d\d| \d) \d\d\d\d (\d\d| \d):\d\d:\d\d)\s+({host}[\w\.-]+)\s*:\s*%ASA-""",
    """(\w{3} \d\d \d\d:\d\d:\d\d)\s+({host}[\w\.-]+)\s*%ASA""",
    """%ASA-({priority}\d+)-({event_code}\d+)""",
    """({event_name}access-list\s*(.+?)\s*({action}permitted|denied|est-allowed)\s*({protocol}\S+))"""
# acl is removed
    """\sfor user\s*'({user}.+?)'\s""",
    """\s({src_interface}[^\s\/]+)/(({src_ip}(\d{1,3}\.){3}\d{1,3}|([A-Fa-f0-9%.]*:[A-Fa-f0-9%.:]+(th0)?))|({src_host}[^\s]+?))(\(({src_port}\d+)\))?\s+->\s+({dest_interface}[^\s\/]+)/(({dest_ip}(\d{1,3}\.){3}\d{1,3}|([A-Fa-f0-9%.]*:[A-Fa-f0-9%.:]+(th0)?))|({dest_host}[^\s]+?))(\(({dest_port}\d+)\))?""",
"""\shit-cnt\s+({hit_cnt}\d+)\s+(first hit|\d+)""", # interval is removed
# DL Field are removed
  ]


}
```