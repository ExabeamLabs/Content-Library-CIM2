#### Parser Content
```Java
{
Name = infoblox-bddi-kv-dns-record-modify-success-mxrecord
  Vendor = Infoblox
  Product = BloxOne DDI
  TimeFormat = "yyyy-MM-dd HH:mm:ss.SSS"
  Conditions = [ """ httpd: """, """]: Modified MxRecord """, """DnsView=""", """exchanger=""" ]
  Fields = [
    """\d\d:\d\d:\d\d\s({host}\S+)\s""",
    """: ({time}\d{4}-\d\d-\d\d\s\d\d:\d\d:\d\d\.\d\d\d)""",
    """({operation}Modified MxRecord)""",
# name_server is removed
# dns_view is removed
# exchanger is removed
# new_ttl is removed
# use_ttl is removed
# new_priority is removed
  ]
  ParserVersion = "v1.0.0"


}
```