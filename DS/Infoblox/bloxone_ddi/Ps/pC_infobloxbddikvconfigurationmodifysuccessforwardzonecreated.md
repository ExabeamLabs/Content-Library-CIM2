#### Parser Content
```Java
{
Name = infoblox-bddi-kv-configuration-modify-success-forwardzonecreated
  Vendor = Infoblox
  Product = BloxOne DDI
  TimeFormat = "yyyy-MM-dd HH:mm:ss.SSS"
  Conditions = [ """ httpd: """, """]: Created ForwardZone """ ]
  Fields = [
    """\d\d:\d\d:\d\d\s({host}\S+)\s""",
    """: ({time}\d{4}-\d\d-\d\d\s\d\d:\d\d:\d\d\.\d\d\d)""",
    """({operation}Created ForwardZone)""",
# forwardzone is removed
# comment is removed
# fqdn is removed
# zone_format is removed
# locked is removed
# disabled is removed
# forward_to is removed
# forwarding_servers is removed
# forwarders_only is removed
# ns_group is removed
# ns_group_external is removed
  ]
  ParserVersion = "v1.0.0"


}
```