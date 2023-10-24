#### Parser Content
```Java
{
Name = infoblox-bddi-kv-dns-record-delete-success-mxrecord
  Vendor = Infoblox
  Product = BloxOne DDI
  TimeFormat = "yyyy-MM-dd HH:mm:ss.SSS"
  Conditions = [ """ httpd: """, """]: Deleted MxRecord """, """DnsView=""", """exchanger=""" ]
  Fields = [
    """\d\d:\d\d:\d\d\s({host}\S+)\s""",
    """: ({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d\.\d\d\d)""",
    """({operation}Deleted MxRecord)""",
# name_server is removed
# dns_view is removed
# exchanger is removed
  ]
  ParserVersion = "v1.0.0"


}
```