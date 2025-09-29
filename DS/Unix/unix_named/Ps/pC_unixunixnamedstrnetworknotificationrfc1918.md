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
    """client (@\dx[0-9a-fA-F]+)?\s*((({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))|({src_host}[\w\-.]+))(#({src_port}\d+))?).+?Internet for ({dns_query}\S+)""",
    """({event_name}RFC 1918 response from Internet)""",
    """\s+({process_name}\S+)\[({process_id}\d+)\]\:\s*"""
  ]
  ParserVersion = "v1.0.0"


}
```