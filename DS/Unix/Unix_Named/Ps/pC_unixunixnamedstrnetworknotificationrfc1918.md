#### Parser Content
```Java
{
Name = unix-unixnamed-str-network-notification-rfc1918
  Vendor = Unix
  Product = Unix Named
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """RFC 1918 response from Internet""" ]
  Fields = [
    """\d\d:\d\d:\d\d ({host}\S+) named""",
    """client ({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}).+?Internet for ({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})""",
    """({event_name}RFC 1918 response from Internet)""",
  ]
  ParserVersion = "v1.0.0"


}
```