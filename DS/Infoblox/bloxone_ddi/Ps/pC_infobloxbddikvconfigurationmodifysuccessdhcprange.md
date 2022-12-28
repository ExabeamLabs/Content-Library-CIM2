#### Parser Content
```Java
{
Name = infoblox-bddi-kv-configuration-modify-success-dhcprange
  Vendor = Infoblox
  Product = BloxOne DDI
  TimeFormat = "yyyy-MM-dd HH:mm:ss.SSS"
  Conditions = [ """ httpd: """, """]: Modified DhcpRange """, """end_address=""", """start_address=""" ]
  Fields = [
    """\d\d:\d\d:\d\d\s({host}\S+)\s""",
    """: ({time}\d{4}-\d\d-\d\d\s\d\d:\d\d:\d\d\.\d\d\d)""",
    """({operation}Modified DhcpRange)""",
# dhcp_range is removed
# new_start_address is removed
# new_end_address is removed
  ]
  ParserVersion = "v1.0.0"


}
```