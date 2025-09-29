#### Parser Content
```Java
{
Name = "infoblox-nios-kv-app-notification-failure"
  ParserVersion = "v1.0.0"
  Vendor = "Infoblox"
  Product = "Infoblox NIOS"
  TimeFormat = ["yyyy-MM-dd'T'HH:mm:ssZ", "MMM dd HH:mm:ss"]
  Conditions = [ """ monitor[""", """Event: A named daemon monitoring failure has occurred.""" ]
  Fields = [
    """({time}\w+\s+\d+ \d+:\d+:\d+)"""
    """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d(\+|\-)\d\d:\d\d)""",
    """\d\d:\d\d:\d\d\s({host}\S+)\s""",
    """({operation}Event: A named daemon monitoring failure has occurred.)""",
    """Type: ({event_category}[^,\s]+)""",
    """State: ({status_msg}[^,\s]+)""",
  ]


}
```