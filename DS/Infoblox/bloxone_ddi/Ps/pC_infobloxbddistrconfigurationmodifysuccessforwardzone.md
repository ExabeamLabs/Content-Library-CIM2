#### Parser Content
```Java
{
Name = infoblox-bddi-str-configuration-modify-success-forwardzone
  Vendor = Infoblox
  Product = BloxOne DDI
  TimeFormat = "yyyy-MM-dd HH:mm:ss.SSS"
  Conditions = [ """ httpd: """, """]: Deleted ForwardZone """, """DnsView=""" ]
  Fields = [
    """\d\d:\d\d:\d\d\s({host}\S+)\s""",
    """: ({time}\d{4}-\d\d-\d\d\s\d\d:\d\d:\d\d\.\d\d\d)""",
    """({operation}Deleted ForwardZone)""",
# forwardzone is removed
# dns_view is removed
  ]
  DupFields = ["operation->event_name"]
  ParserVersion = "v1.0.0"


}
```