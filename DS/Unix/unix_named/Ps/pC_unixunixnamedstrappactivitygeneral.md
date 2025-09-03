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
    """client ({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))\#({src_port}\d+)""",
    """: general: (zone ({zone}[^:]+):)?\s*({event_name}.+?)\s+$""",
  ]


}
```