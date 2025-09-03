#### Parser Content
```Java
{
Name = unix-unixnamed-str-dns-request-success-client-1
Vendor = Unix
Product = Unix Named
TimeFormat = "dd-MMM-yyyy HH:mm:ss.SSS"
Conditions = [
  """ query: """
  """ info: client """
  """ named["""
  """queries:"""
]
Fields = [
  """({time}\d\d-\w+-\d\d\d\d \d\d:\d\d:\d\d\.\d\d\d)"""
  """client\s*({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})\#({src_port}\d+)"""
  """query:\s*({dns_query}[^\s]+)"""
  """query:\s*({dns_query}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})"""
  """\sIN\s({dns_query_type}[^\s]+)\s+({dns_query_flags}[^"\s]+)"""
]
ParserVersion = "v1.0.0"


}
```