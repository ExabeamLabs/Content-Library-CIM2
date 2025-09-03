#### Parser Content
```Java
{
Name = infoblox-nios-str-app-notification-recursionclient
  Vendor = Infoblox
  Product = Infoblox NIOS
  TimeFormat = ["yyyy-MM-dd'T'HH:mm:ssZ", "MMM dd HH:mm:ss"]
  Conditions = [ """ named[""", """]: Recursion client quota: """ ]
  Fields = [
    """({time}\w+\s+\d+ \d+:\d+:\d+)"""
    """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d(\+|\-)\d\d:\d\d)""",
    """\d\d:\d\d:\d\d\s({host}\S+)\s""",
    """]: ({event_name}Recursion client quota: .+?)\s*$""",
  ]
  ParserVersion = "v1.0.0"


}
```