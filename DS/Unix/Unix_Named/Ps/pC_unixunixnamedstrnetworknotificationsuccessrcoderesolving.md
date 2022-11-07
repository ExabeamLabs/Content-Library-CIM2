#### Parser Content
```Java
{
Name = unix-unixnamed-str-network-notification-success-rcoderesolving
  ParserVersion = v1.0.0
  Vendor = Unix
  Product = Unix Named
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """unexpected RCODE resolving""" ]
  Fields = [
    """\d\d:\d\d:\d\d ({host}\S+) named""",
    """({result}\S+)\s+({event_name}unexpected RCODE resolving)\s+\'((({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})[^\']+?)|(({dest_host}[\w\-.]+)[^\']+?))\':\s*({name_server}[^\s\#]+)\#""",
  ]


}
```