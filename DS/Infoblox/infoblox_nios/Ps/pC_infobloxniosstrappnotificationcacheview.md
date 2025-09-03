#### Parser Content
```Java
{
Name = infoblox-nios-str-app-notification-cacheview
  Vendor = Infoblox
  Product = Infoblox NIOS
  ParserVersion = "v1.0.0"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
  Conditions = [ """ named[""", """]: Recursion cache view """, """size = """, """hits = """, """misses = """ ]
  Fields = [
    """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d(\+|\-)\d\d:\d\d)""",
    """\d\d:\d\d:\d\d\s({host}\S+)\s""",
    """]: ({event_name}Recursion cache view [^:]+)""",
# size is removed
# hits is removed
# misses is removed
  ]


}
```