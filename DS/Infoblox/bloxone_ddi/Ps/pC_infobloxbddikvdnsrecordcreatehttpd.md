#### Parser Content
```Java
{
Name = infoblox-bddi-kv-dns-record-create-httpd
  ParserVersion = v1.0.0
  Vendor = Infoblox
  Product = BloxOne DDI
  TimeFormat = "yyyy-MM-dd HH:mm:ss.SSS"
  Conditions = [ """ httpd: """, """]: Created HostAddress """, """address=""", """: Set""" ]
  Fields = [
    """\d\d:\d\d:\d\d\s({host}\S+)\s""",
    """: ({time}\d{4}-\d\d-\d\d\s\d\d:\d\d:\d\d\.\d\d\d)""",
    """({operation}Created HostAddress)""",
    """Created HostAddress ({server}\S+)\s""",
# host_record is removed
# reserved_interface is removed
  ]
  DupFields = ["operation->event_name"]


}
```