#### Parser Content
```Java
{
Name = infoblox-bddi-kv-dns-record-create-success-exchanger
  Vendor = Infoblox
  Product = BloxOne DDI
  TimeFormat = "yyyy-MM-dd HH:mm:ss.SSS"
  Conditions = [ """ httpd: """, """]: Created MxRecord """, """DnsView=""", """exchanger=""", """: Set""" ]
  Fields = [
    """\d\d:\d\d:\d\d\s({host}\S+)\s""",
    """: ({time}\d{4}-\d\d-\d\d\s\d\d:\d\d:\d\d\.\d\d\d)""",
    """({operation}Created MxRecord)""",
# name_server is removed
# dns_view is removed
# exchanger is removed
# ddns_principal is removed
# fqdn is removed
    """priority=({priority}\d+)""",
# comment is removed
  ]
  ParserVersion = "v1.0.0"


}
```