#### Parser Content
```Java
{
Name = cisco-asa-str-network-session-fail-710003
  ParserVersion = v1.0.0
  Vendor = Cisco
  Product = Cisco Adaptive Security Appliance
  TimeFormat = "MMM dd yyyy HH:mm:ss"
  Conditions = [ """-710003""", """%ASA-""" ]
  Fields = [
    """({time}\w{3} \d\d \d\d\d\d \d\d:\d\d:\d\d)\s*(::ffff:)?({host}[\w\-.]+)?\s*:\s*%ASA""",
    """(::ffff:)?({host}[\w\-.]+)\s+({time}\w+ \d\d \d\d\d\d \d\d:\d\d:\d\d):\s*%ASA""",
    """%ASA-({priority}\d+)""",
    """({event_code}710003)""",
    """({protocol}\S+?) ({event_name}access denied by ACL)""",
    """ from ((::ffff:)?({src_ip}(\d{1,3}\.){3}\d{1,3}|([A-Fa-f0-9%.]*:[A-Fa-f0-9%.:]+(th0)?))|(::ffff:)?({src_host}[^\s]+?))\/({src_port}\d+) to ({dest_interface}\S+?)\s*:\s*((::ffff:)?({dest_ip}(\d{1,3}\.){3}\d{1,3}|([A-Fa-f0-9%.]*:[A-Fa-f0-9%.:]+(th0)?))|(::ffff:)?({dest_host}[^\s]+?))\/({dest_port}\d+)"""
  ]


}
```