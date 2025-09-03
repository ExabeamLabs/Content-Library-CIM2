#### Parser Content
```Java
{
Name = infoblox-bddi-kv-configuration-modify-success-canonicalname
  Vendor = Infoblox
  Product = BloxOne DDI
  TimeFormat = "yyyy-MM-dd HH:mm:ss.SSS"
  Conditions = [ """ httpd: """, """]: Created CnameRecord """, """DnsView=""", """canonical_name=""", """: Set""" ]
  Fields = [
    """\d\d:\d\d:\d\d\s({host}\S+)\s""",
    """: ({time}\d{4}-\d\d-\d\d\s\d\d:\d\d:\d\d\.\d\d\d)""",
    """({operation}Created CnameRecord)""",
# name_server is removed
    """canonical_name="({cname}[^"]+)"""",
# fqdn is removed
# comment is removed
  ]
  DupFields = ["operation->event_name"]
  ParserVersion = "v1.0.0"


}
```