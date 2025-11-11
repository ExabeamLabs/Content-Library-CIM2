#### Parser Content
```Java
{
Name = "f5-bigipdns-str-dns-response-success-to"
Vendor = "F5"
Product = "F5 BIG-IP DNS"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
""" qid """
""" to """
""" response:"""
]
Fields = [
"""({time}\d\d\d\d-\d\d-\d\d (\d\d| \d):\d\d:\d\d)\s+({host}({src_host}[\w\.-]+))\s+qid"""
"""({host}({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})))(:({src_port}\d+))?\s+qid"""
"""\s({host}({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})))(:({src_port}\d+))?\s+qid"""
"""qid\s+({query_id}\d+)\s+to\s+({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(#({dest_port}\d+))?:"""
"""\[({dns_response_code}\S+)\s+({dns_response_flags}.+?)\]\s+response:"""
"""response:\s*({dns_query}[^\s]+)\s?({response_ttl}\d+)\s+IN\s+({dns_query_type}[^\s]+)\s+({dns_response}[^\s]+);"""
"""response:\s*({full_response}.+?)\s*$"""
]
ParserVersion = "v1.0.0"


}
```