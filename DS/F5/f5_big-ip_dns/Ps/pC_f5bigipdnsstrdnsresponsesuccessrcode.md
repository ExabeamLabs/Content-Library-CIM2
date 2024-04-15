#### Parser Content
```Java
{
Name = "f5-bigipdns-str-dns-response-success-rcode"
Vendor = "F5"
Product = "F5 BIG-IP DNS"
TimeFormat = "yyyy-MM-dd HH:mm:ssZ"
Conditions = [
""" q="""
""" rcode="""
"""IN"""
""" anslen="""
]
Fields = [
"""({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\dZ)"""
"""\ssrc=({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
"""\sq=({dns_query}[^\s]+)"""
"""\st=({dns_query_type}\w+)\s*"""
"""\srcode=({dns_response_code}\w+)"""
"""\sans=\"[^\";]*?IN\s+\S+\s+({dns_response}[^\"\s;]+)"""
"""\sans=\"({response_full}[^\"]+)\""""
]
ParserVersion = "v1.0.0"


}
```