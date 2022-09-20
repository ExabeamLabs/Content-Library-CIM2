#### Parser Content
```Java
{
Name = unix-unixnamed-str-app-activity-updatesecurity
  ParserVersion = v1.0.0
  Vendor = Unix
  Product = Unix Named
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """ named[""", """update-security: client""" ]
  Fields = [
    """\w+\s+\d+\s+\d\d:\d\d:\d\d\s+({host}\S+)\s+named\[""",
    """client ({src_ip}[A-Fa-f:\d.]+)\#({src_port}\d+)""",
    """update-security: ({event_name}[^']*?(\'({query}[^\'\/]+)[^']*')?[^']*?)\s+$""",
  ]


}
```