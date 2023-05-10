#### Parser Content
```Java
{
Name = unix-unixnamed-str-app-activity-success-lameservers
  Vendor = Unix
  Product = Unix Named
  ParserVersion = "v1.0.0"
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """ named[""", """: lame-servers: """ ]
  Fields = [
    """\w+\s+\d+\s+\d\d:\d\d:\d\d\s+({host}\S+)\s+named\[""",
    """({src_ip}[A-Fa-f:\d.]+)\#({src_port}\d+)""",
    """: lame-servers: ({event_name}[^']*?)\s*'({query}[^'\/]+)""",
  ]


}
```