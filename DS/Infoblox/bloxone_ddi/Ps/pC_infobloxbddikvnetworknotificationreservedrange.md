#### Parser Content
```Java
{
Name = infoblox-bddi-kv-network-notification-reservedrange
  ParserVersion = v1.0.0
  Vendor = Infoblox
  Product = BloxOne DDI
  TimeFormat = "yyyy-MM-dd HH:mm:ss.SSS"
  Conditions = [ """ httpd: """, """]: Created ReservedRange """ ]
  Fields = [
    """\d\d:\d\d:\d\d\s({host}\S+)\s""",
    """: ({time}\d{4}-\d\d-\d\d\s\d\d:\d\d:\d\d\.\d\d\d)""",
    """({operation}Created ReservedRange)""",
# reservedrange is removed
# dns_view is removed
# comment is removed
# enable_discovery is removed
# enable_immediate_discovery is removed
# end_address is removed
    """name="({name}[^"]+)""",
# start_address is removed
# use_basic_polling_settings is removed
# use_member_enable_discovery is removed
# parent is removed
  ]


}
```