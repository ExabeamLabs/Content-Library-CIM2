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
    """({event_name}timed out resolving)\s+\'({dns_query}[^'\/]+?)\/({dns_query_type}[^'\/]+?)\/.*?\':\s*({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))\#({dest_port}\d+)""", # name_server is removed
  ]


}
```