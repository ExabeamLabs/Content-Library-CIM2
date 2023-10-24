#### Parser Content
```Java
{
Name = unix-unixnamed-str-app-notification-lameserverresolving
  Vendor = Unix
  Product = Unix Named
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """lame server resolving""" ]
  Fields = [
    """\d\d:\d\d:\d\d ({host}\S+) named""",
    """lame server resolving \'((({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})[^\']+?)|({dest_host}[\w\-.]+))\' \([^\)]+\):\s*([^\s\#]+)\#""", # name_server is removed
    """({event_name}lame server resolving)""",
  ]
  ParserVersion = "v1.0.0"


}
```