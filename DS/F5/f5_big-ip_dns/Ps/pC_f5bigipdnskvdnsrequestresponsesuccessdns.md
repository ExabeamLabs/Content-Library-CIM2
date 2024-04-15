#### Parser Content
```Java
{
Name = "f5-bigipdns-kv-dns-request-response-success-dns"
Vendor = "F5"
Product = "F5 BIG-IP DNS"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
Conditions = [
""",F5 DNS """
""",question_name="""
""",question_type="""
]
Fields = [
    """"@timestamp":"({time}\d\d\d\d-\d\d-\d\dT\d+:\d+:\d+\.\d+Z)""",
    """,src_ip=({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """,dns_server_ip=({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """,question_name=({dns_query}[^,]+),"""
    """,question_name=({query_1}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})({query_2}[^,]*)""",
    """,question_type=({dns_query_type}[^,"]+)"*,"""

]
ParserVersion = "v1.0.0"


}
```