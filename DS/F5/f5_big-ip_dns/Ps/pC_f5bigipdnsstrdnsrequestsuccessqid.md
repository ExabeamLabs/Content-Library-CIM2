#### Parser Content
```Java
{
Name = "f5-bigipdns-str-dns-request-success-qid"
Vendor = "F5"
Product = "F5 BIG-IP DNS"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
""" qid """
""" from """
""" query:"""
""" IN """
]
Fields = [
"""({time}\d\d\d\d-\d\d-\d\d (\d\d| \d):\d\d:\d\d)\s+({host}[\w\.-]+)\s+qid"""
"""qid\s+({query_id}\d+)\s+from\s+({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(#({src_port}\d+))?:"""
""":\s*view\s+({view}.+?)\s*:"""
"""query:\s*({dns_query}[^\s]+)\s*IN\s+({dns_query_type}[^\s]+)\s+({dns_query_flags}[^\s]+)\s*(\(({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?(%\d+?)\))?"""
]
ParserVersion = "v1.0.0"


}
```