#### Parser Content
```Java
{
Name = unix-unixnamed-str-app-notification-networkunreachable
  Vendor = Unix
  Product = Unix Named
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """named[""", """network unreachable resolving""" ]
  Fields = [
    """\d\d:\d\d:\d\d ({host}\S+) named""",
    """({event_name}network unreachable resolving)\s+\'((({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})[^\']+?)|(({dest_host}[\w\-.]+)[^\']+?))\':\s*([^\s\#]+)\#""", # name_server is removed
  ]
  ParserVersion = "v1.0.0"


}
```