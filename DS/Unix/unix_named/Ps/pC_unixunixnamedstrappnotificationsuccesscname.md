#### Parser Content
```Java
{
Name = unix-unixnamed-str-app-notification-success-cname
  Vendor = Unix
  Product = Unix Named
  ParserVersion = "v1.0.0"
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """ named[""", """: cname: """ ]
  Fields = [
    """\w+\s+\d+\s+\d\d:\d\d:\d\d\s+({host}\S+)\s+named\[""",
    """: cname: ({event_name}.*?nameserver '([^\']+)'.*?'({dns_query}[^\'\/]+).*?)\s+$""", # name_server is removed
  ]


}
```