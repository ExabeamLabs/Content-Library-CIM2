#### Parser Content
```Java
{
Name = unix-unixnamed-str-app-notification-resolving
  Vendor = Unix
  Product = Unix Named
  ParserVersion = "v1.0.0"
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """named[""", """timed out resolving""" ]
  Fields = [
    """\d\d:\d\d:\d\d ({host}\S+) named""",
    """({event_name}timed out resolving)\s+\'((({dest_ip}\d+\.\d+\.\d+\.\d+)[^\']+?)|(({dest_host}[\w\-.]+)[^\']+?))\':\s*([^\s\#]+)\#""", # name_server is removed
  ]


}
```