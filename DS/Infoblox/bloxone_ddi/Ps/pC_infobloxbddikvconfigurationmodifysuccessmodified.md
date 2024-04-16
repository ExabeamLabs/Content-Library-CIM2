#### Parser Content
```Java
{
Name = infoblox-bddi-kv-configuration-modify-success-modified
  Vendor = Infoblox
  Product = BloxOne DDI
  TimeFormat = "yyyy-MM-dd HH:mm:ss.SSS"
  Conditions = [ """ httpd: """, """]: Modified ForwardZone """ ]
  Fields = [
    """\d\d:\d\d:\d\d\s({host}\S+)\s""",
    """: ({time}\d{4}-\d\d-\d\d\s\d\d:\d\d:\d\d\.\d\d\d)""",
    """({operation}Modified ForwardZone)""",
# forwardzone is removed
  ]
  DupFields = ["operation->event_name"]
  ParserVersion = "v1.0.0"


}
```