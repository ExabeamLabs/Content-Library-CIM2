#### Parser Content
```Java
{
Name = infoblox-bddi-kv-dns-record-modify-httpd-1
  ParserVersion = v1.0.0
  Vendor = Infoblox
  Product = BloxOne DDI
  TimeFormat = "yyyy-MM-dd HH:mm:ss.SSS"
  Conditions = [ """ httpd: """, """]: Modified ARecord """, """DnsView=""", """address=""" ]
  Fields = [
    """\d\d:\d\d:\d\d\s({host}\S+)\s""",
    """: ({time}\d{4}-\d\d-\d\d\s\d\d:\d\d:\d\d\.\d\d\d)""",
    """({operation}Modified ARecord)""",
# name_server is removed
# dns_view is removed
# new_host_record is removed
  ]


}
```