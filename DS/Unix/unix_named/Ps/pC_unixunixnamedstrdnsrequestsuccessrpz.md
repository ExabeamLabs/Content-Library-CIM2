#### Parser Content
```Java
{
Name = unix-unixnamed-str-dns-request-success-rpz
Vendor = Unix
Product = Unix Named
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
  """: rpz """
  """]: client """
  """ named["""
  """ rewrite """
  """.rpz."""
]
Fields = [
  """\d\d:\d\d:\d\d ({host}\S+) named"""
  """client\s[^\s]+?\s({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})\#({src_port}\d+)\s\(({dns_query}[^)]+)"""
  """rpz ({triggers}[^\s]+)\s({action}[^\s]+)\s"""
  """({event_name}rewrite)"""
]
ParserVersion = "v1.0.0"


}
```