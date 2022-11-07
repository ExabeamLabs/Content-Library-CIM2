#### Parser Content
```Java
{
Name = unix-unixnamed-str-app-activity-general
  ParserVersion = v1.0.0
  Vendor = Unix
  Product = Unix Named
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """ named[""", """: general: """ ]
  Fields = [
    """\w+\s+\d+\s+\d\d:\d\d:\d\d\s+({host}\S+)\s+named\[""",
    """client ({src_ip}[A-Fa-f:\d.]+)\#({src_port}\d+)""",
    """: general: (zone ({zone}[^:]+):)?\s*({event_name}.+?)\s+$""",
  ]


}
```