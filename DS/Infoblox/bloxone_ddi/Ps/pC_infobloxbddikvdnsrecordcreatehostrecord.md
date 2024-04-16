#### Parser Content
```Java
{
Name = infoblox-bddi-kv-dns-record-create-hostrecord
  Vendor = Infoblox
  Product = BloxOne DDI
  ParserVersion = "v1.0.0"
  TimeFormat = "yyyy-MM-dd HH:mm:ss.SSS"
  Conditions = [ """ httpd: """, """]: Created HostRecord """, """DnsView=""", """address=""", """: Set""" ]
  Fields = [
    """\d\d:\d\d:\d\d\s({host}\S+)\s""",
    """: ({time}\d{4}-\d\d-\d\d\s\d\d:\d\d:\d\d\.\d\d\d)""",
    """({operation}Created HostRecord)""",
# name_server is removed
# dns_view is removed
# host_record is removed
# ddns_protected is removed
# fqdn is removed
# comment is removed
  ]
  DupFields = ["operation->event_name"]


}
```