#### Parser Content
```Java
{
Name = "infoblox-nios-kv-app-notification-failure"
  ParserVersion = "v1.0.0"
  Vendor = "Infoblox"
  Product = "Infoblox NIOS"
  TimeFormat = "yyyy-MM-dd HH:mm:ss.SSS"
  Conditions = [ """ monitor[""", """Event: A named daemon monitoring failure has occurred.""" ]
  Fields = [
    """\d\d:\d\d:\d\d\s({host}\S+)\s""",
    """({operation}Event: A named daemon monitoring failure has occurred.)""",
    """Type: ({event_category}[^,\s]+)""",
    """State: ({state}[^,\s]+)""",
  ]


}
```