#### Parser Content
```Java
{
Name = cisco-asa-str-network-session-fail-10610
  ParserVersion = v1.0.0
  Vendor = Cisco
  Product = Cisco Adaptive Security Appliance
  TimeFormat = ["MMM dd yyyy HH:mm:ss", "MMM dd HH:mm:ss", "yyyy-MM-dd'T'HH:mm:ss.SSSZ"]
  Conditions = [ """%ASA-""", """-10610""", """: access-list """, """hit-cnt""" ]
  Fields = [
    """({time}\d{4}\-\d{2}\-\d{2}T\d{2}:\d{2}:\d{2}\.\d+((\+|\-)\d\d:\d\d)?)\s+""",
    """\s(({host}[\w.\-]+))\s+([-\s:]+)?%ASA""",
    """({time}\w+ \d\d (\d\d\d\d )?\d\d:\d\d:\d\d)""",
    """(\w{3} (\d\d| \d) \d\d\d\d (\d\d| \d):\d\d:\d\d)\s+({host}[\w\.-]+)\s*:\s*%ASA-""",
    """\d\d:\d\d:\d\d\s+(::ffff:)?((?i)system|({host}[\w\.-]+))[\s:]+%ASA-""",
    """%ASA-({priority}\d+)-({event_code}\d+)""",
    """({event_name}access-list\s*({access_list}.+?)\s*({action}permitted|denied|est-allowed)\s*({protocol}\S+))"""
    """({failure_reason}access-list\s*(.+?)\s*denied\s*)"""
    """\sfor user\s*'(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-]{1,40}\$?))'""",
    """\s({src_interface}[^\s\/]+)/(({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})|([A-Fa-f0-9%.]*:[A-Fa-f0-9%.:]+(th0)?))|({src_host}[^\s]+?))(\(({src_port}\d+)\))?\s+->\s+({dest_interface}[^\s\/]+)/(({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})|([A-Fa-f0-9%.]*:[A-Fa-f0-9%.:]+(th0)?))|({dest_host}[^\s]+?))(\(({dest_port}\d+)\))?""",
"""\shit-cnt\s+({hit_cnt}\d+)\s+(first hit|\d+)""", # interval is removed
"""->\s*outside\/({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))\(({dest_port}\d+)\)"""
# DL Field are removed
  ]


}
```