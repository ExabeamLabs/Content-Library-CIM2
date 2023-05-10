#### Parser Content
```Java
{
Name = cisco-asa-str-network-traffic-fail-313001
  ParserVersion = v1.0.0
  Vendor = Cisco
  Product = Cisco Adaptive Security Appliance
  TimeFormat = "MMM dd yyyy HH:mm:ss"
  Conditions = [ """-313001""", """%ASA-""", """Denied """ ]
  Fields = [
    """({time}\w+ \d+ \d{4} \d\d:\d\d:\d\d)""",
    """Original Address=(::ffff:)?({host}\S+) ({time}\w+ \d+ \d\d\d\d \d\d:\d\d:\d\d) (::ffff:)?({=host}[\w\-.]+)""",
    """%ASA-({priority}\d+)-({event_code}\d+)""",
    """({event_name}Denied ({protocol}\w+))\s""",
    """\sfrom\s*((::ffff:)?({src_ip}(\d{1,3}\.){3}\d{1,3}|([A-Fa-f0-9%.]*:[A-Fa-f0-9%.:]+(th0)?))|(::ffff:)?({src_host}[^\s]+?))\s*on interface\s({src_interface}\w+)"""
  ]


}
```