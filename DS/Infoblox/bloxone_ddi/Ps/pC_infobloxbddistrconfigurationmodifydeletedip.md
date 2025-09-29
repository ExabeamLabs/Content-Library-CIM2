#### Parser Content
```Java
{
Name = infoblox-bddi-str-configuration-modify-deletedip
  ParserVersion = v1.0.0
  Vendor = Infoblox
  Product = BloxOne DDI
  TimeFormat = "yyyy-MM-dd HH:mm:ss.SSS"
  Conditions = [ """ httpd: """, """]: Deleted IPv4Address """, """network_view=""" ]
  Fields = [
    """\d\d:\d\d:\d\d\s({host}\S+)\s""",
    """: ({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d\.\d\d\d)""",
    """({operation}Deleted IPv4Address)""",
    """({event_name}Deleted IPv4Address) ({ipv4_address_deleted}\S+)\s""",
    """\s+({process_name}\S+)\[({process_id}\d+)\]\:\s*"""
# network_view is removed
  ]


}
```