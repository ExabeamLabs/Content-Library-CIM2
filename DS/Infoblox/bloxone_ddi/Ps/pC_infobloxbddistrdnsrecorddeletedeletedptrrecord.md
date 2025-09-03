#### Parser Content
```Java
{
Name = infoblox-bddi-str-dns-record-delete-deletedptrrecord
  ParserVersion = v1.0.0
  Vendor = Infoblox
  Product = BloxOne DDI
  TimeFormat = "yyyy-MM-dd HH:mm:ss.SSS"
  Conditions = [ """ httpd: """, """]: Deleted PtrRecord """, """DnsView=""", """address=""" ]
  Fields = [
    """\d\d:\d\d:\d\d\s({host}\S+)\s""",
    """: ({time}\d{4}-\d\d-\d\d\s\d\d:\d\d:\d\d\.\d\d\d)""",
    """({operation}Deleted PtrRecord)""",
# ptrrecord is removed
# dns_view is removed
# address is removed
# dname is removed
  ]
  DupFields = ["operation->event_name"]


}
```