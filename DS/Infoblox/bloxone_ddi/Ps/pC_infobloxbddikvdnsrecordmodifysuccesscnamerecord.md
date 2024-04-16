#### Parser Content
```Java
{
Name = infoblox-bddi-kv-dns-record-modify-success-cnamerecord
  Vendor = Infoblox
  Product = BloxOne DDI
  TimeFormat = "yyyy-MM-dd HH:mm:ss.SSS"
  Conditions = [ """ httpd: """, """]: Modified CnameRecord """ ]
  Fields = [
    """\d\d:\d\d:\d\d\s({host}\S+)\s""",
    """: ({time}\d{4}-\d\d-\d\d\s\d\d:\d\d:\d\d\.\d\d\d)""",
    """({operation}Modified CnameRecord)""",
# cnamerecord is removed
# dns_view is removed
# new_cname is removed
  ]
  DupFields = ["operation->event_name"]
  ParserVersion = "v1.0.0"


}
```