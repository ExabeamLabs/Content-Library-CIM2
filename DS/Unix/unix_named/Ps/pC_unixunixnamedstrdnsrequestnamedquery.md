#### Parser Content
```Java
{
Name = unix-unixnamed-str-dns-request-namedquery
  Vendor = Unix
  Product = Unix Named
  TimeFormat = "dd-MMM-yyyy HH:mm:ss.SSS"
  Conditions = [ """: query """, """named[""" ]
  Fields = [
    """\d\d:\d\d:\d\d ({host}[\w\-.]+?)\s+named\[""",
    """client\s*(@[^\s]+)?\s*({src_ip}\d{1,3}.\d{1,3}.\d{1,3}.\d{1,3})\#({src_port}\d+)""",
    """query\s*.+?(\([^\)]*\))?(for)?\s*'?({dns_query}[^\s'\/]+)\/({dns_query_type}[^\/']+)[^']*'?\s*({result}\S+)""",
    """query ({result}failed)\s*(\([^\)]*\))?\s*for ({dns_query}[^\s'\/]+)\/(?:[^\/']+)\/({dns_query_type}[^\s]+) at"""
    """\s+({process_name}\S+)\[({process_id}\d+)\]\:\s*"""
  ]
  ParserVersion = "v1.0.0"


}
```