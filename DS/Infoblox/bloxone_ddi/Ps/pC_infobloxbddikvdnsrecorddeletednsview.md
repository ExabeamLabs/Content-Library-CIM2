#### Parser Content
```Java
{
Name = infoblox-bddi-kv-dns-record-delete-dnsview
  ParserVersion = v1.0.0
  Vendor = Infoblox
  Product = BloxOne DDI
  TimeFormat = "yyyy-MM-dd HH:mm:ss.SSS"
  Conditions = [ """ httpd: """, """]: Deleted ARecord """, """DnsView=""", """address=""" ]
  Fields = [
    """\d\d:\d\d:\d\d\s({host}\S+)\s""",
    """: ({time}\d{4}-\d\d-\d\d\s\d\d:\d\d:\d\d\.\d\d\d)""",
    """({operation}Deleted ARecord)""",
# arecord is removed
# dns_view is removed
# address is removed
# remove_associated_ptr is removed
  ]


}
```