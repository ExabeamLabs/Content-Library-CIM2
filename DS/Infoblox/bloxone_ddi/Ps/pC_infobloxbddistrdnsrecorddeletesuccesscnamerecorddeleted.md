#### Parser Content
```Java
{
Name = infoblox-bddi-str-dns-record-delete-success-cnamerecorddeleted
  Vendor = Infoblox
  Product = BloxOne DDI
  TimeFormat = "yyyy-MM-dd HH:mm:ss.SSS"
  Conditions = [ """ httpd: """, """]: Deleted CnameRecord """, """DnsView=""" ]
  Fields = [
    """\d\d:\d\d:\d\d\s({host}\S+)\s""",
    """: ({time}\d{4}-\d\d-\d\d\s\d\d:\d\d:\d\d\.\d\d\d)""",
    """({operation}Deleted CnameRecord)""",
# name_server is removed
# dns_view is removed
  ]
  ParserVersion = "v1.0.0"


}
```