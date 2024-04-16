#### Parser Content
```Java
{
Name = "infoblox-nios-json-dns-request-success-hostname"
Vendor = "Infoblox"
Product = "Infoblox NIOS"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
Conditions = [
"""infoblox"""
""""hostname":"
""""client_ip":"
""""query_type":"
""""query_name":"
]
Fields = [
"""hostname":\"({host}[\w.-]+)\""""
""""timestamp":\"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\dZ)"""
""""client_ip\\\":\\\"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\\\""""
""""query_type\\\":\\\"({dns_query_type}[^\"]+?)\\\""""
""""query_name\\\":\\\"({dns_query}[^\"]+?)\\\""""
]
ParserVersion = "v1.0.0"


}
```