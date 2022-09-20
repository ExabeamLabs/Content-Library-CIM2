#### Parser Content
```Java
{
Name = infoblox-bddi-kv-dns-record-modify-httpd
  ParserVersion = v1.0.0
  Vendor = Infoblox
  Product = BloxOne DDI
  TimeFormat = "yyyy-MM-dd HH:mm:ss.SSS"
  Conditions = [ """ httpd: """, """]: Modified HostRecord """, """DnsView=""", """Changed""" ]
  Fields = [
    """\d\d:\d\d:\d\d\s({host}\S+)\s""",
    """: ({time}\d{4}-\d\d-\d\d\s\d\d:\d\d:\d\d\.\d\d\d)""",
    """({operation}Modified HostRecord)""",
# name_server is removed
# dns_view is removed
# host_record is removed
  ]


}
```