#### Parser Content
```Java
{
Name = cisco-asa-str-network-session-fail-710003
  ParserVersion = v1.0.0
  Vendor = Cisco
  Product = Cisco Adaptive Security Appliance
  TimeFormat = ["MMM dd yyyy HH:mm:ss", "MMM dd HH:mm:ss", "yyyy-MM-dd'T'HH:mm:ss.SSSZ"]
  Conditions = [ """-710003""", """%ASA-""" ]
  Fields = [
    """({time}\d{4}\-\d{2}\-\d{2}T\d{2}:\d{2}:\d{2}\.\d+((\+|\-)\d\d:\d\d)?)\s+""",
"""\s(({host}[\w.\-]+))\s+([-\s:]+)?%ASA""",
    """({time}\w{3} \d\d (\d\d\d\d )?\d\d:\d\d:\d\d)\s*(::ffff:)?({host}[\w\-.]+)?\s*:?\s*%ASA""",
    """(::ffff:)?({host}[\w\-.]+)\s+({time}\w+ \d\d (\d\d\d\d )?\d\d:\d\d:\d\d):\s*%ASA""",
    """%ASA-({priority}\d+)""",
    """({event_code}710003)""",
    """({failure_reason}({protocol}\S+?) ({event_name}access denied by ACL))""",
    """ from ((::ffff:)?({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})|([A-Fa-f0-9%.]*:[A-Fa-f0-9%.:]+(th0)?))|(::ffff:)?({src_host}[^\s]+?))\/({src_port}\d+) to ({dest_interface}\S+?)\s*:\s*((::ffff:)?({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})|([A-Fa-f0-9%.]*:[A-Fa-f0-9%.:]+(th0)?))|(::ffff:)?({dest_host}[^\s]+?))\/({dest_port}\d+)"""
  ]


}
```