#### Parser Content
```Java
{
Name = infoblox-nios-str-app-notification-recursionclient
  Vendor = Infoblox
  Product = NIOS
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """ named[""", """]: Recursion client quota: """ ]
  Fields = [
    """\d\d:\d\d:\d\d\s({host}\S+)\s""",
    """]: ({event_name}Recursion client quota: .+?)\s*$""",
  ]
  ParserVersion = "v1.0.0"


}
```