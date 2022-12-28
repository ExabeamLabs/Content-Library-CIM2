#### Parser Content
```Java
{
Name = cisco-asa-str-network-traffic-fail-106006
  ParserVersion = v1.0.0
  Vendor = Cisco
  Product = Cisco Adaptive Security Appliance
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """%ASA-""", """-106006""", """Deny """ ]
  Fields = [
    """Original Address=({host}\S+) ({time}\w+ \d+ \d\d\d\d \d\d:\d\d:\d\d) ({=host}[\w\-.]+)""",
    """%ASA-({priority}\d+)-({event_code}\d+)""",
    """({event_name}({action}Deny).+?\s+({protocol}\w+))""",
    """\sfrom\s+(({src_ip}(\d{1,3}\.){3}\d{1,3}|([A-Fa-f0-9%.]*:[A-Fa-f0-9%.:]+(th0)?))|({src_host}[^\s]+?))\/({src_port}\d+)\s+to\s+(({dest_ip}(\d{1,3}\.){3}\d{1,3}|([A-Fa-f0-9%.]*:[A-Fa-f0-9%.:]+(th0)?))|({dest_host}[^\s]+?))\/({dest_port}\d+)\s""",
    """ on interface(\s+({dest_interface}\S+))?"""
  ]


}
```