#### Parser Content
```Java
{
Name = "unix-binddns-str-dns-request-success-query"
Vendor = "Unix"
Product = "BIND DNS"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
Conditions = [
"""[][]"""
"""<CLIENT_DATA>:"""
""" query: """
]
Fields = [
"""<\d+>\d+ ({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d(\+|\-)\d\d:\d\d) ({host}[\w.\-]+)"""
"""({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))\#({src_port}\d+):\s+query:\s+({dns_query}.+?)\s+IN\s+({dns_query_type}\S+)"""
]
ParserVersion = "v1.0.0"


}
```