#### Parser Content
```Java
{
Name = infoblox-bddi-kv-dns-record-create-set
  ParserVersion = v1.0.0
  Vendor = Infoblox
  Product = BloxOne DDI
  TimeFormat = "yyyy-MM-dd HH:mm:ss.SSS"
  Conditions = [ """ httpd: """, """]: Created ARecord """, """DnsView=""", """address=""", """: Set""" ]
  Fields = [
    """\d\d:\d\d:\d\d\s({host}\S+)\s""",
    """: ({time}\d{4}-\d\d-\d\d\s\d\d:\d\d:\d\d\.\d\d\d)""",
# name_server is removed
# dns_view is removed
# host_record is removed
# fqdn is removed
# comment is removed
  ]


}
```