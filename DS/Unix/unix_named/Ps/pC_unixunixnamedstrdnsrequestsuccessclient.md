#### Parser Content
```Java
{
Name = unix-unixnamed-str-dns-request-success-client
Vendor = Unix
Product = Unix Named
TimeFormat = "dd-MMM-yyyy HH:mm:ss.SSS"
Conditions = [
  """ query: """
  """ info: client """
]
Fields = [
  """({time}\d\d-\w+-\d\d\d\d \d\d:\d\d:\d\d\.\d\d\d) info: client ({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})#({src_port}\d+)\s+\((|({dns_query}(\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})|([^\(\)]+))).*?\):\s*query:\s*({=dns_query}(\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})|([^\s]+)).*?\s+IN ({dns_query_type}[^\s]+)\s+({dns_query_flags}.+?)\s*\(({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
  """query:\s*({dns_query}[^\s]+)"""
]
ParserVersion = "v1.0.0"


}
```