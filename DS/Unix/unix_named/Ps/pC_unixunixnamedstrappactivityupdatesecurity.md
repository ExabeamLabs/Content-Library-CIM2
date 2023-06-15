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
    """client ({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))\#({src_port}\d+)""",
    """update-security: ({event_name}[^']*?(\'({query}[^\'\/]+)[^']*')?[^']*?)\s+$""",
  ]


}
```