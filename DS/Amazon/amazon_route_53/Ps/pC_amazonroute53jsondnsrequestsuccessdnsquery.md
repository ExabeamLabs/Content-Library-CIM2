#### Parser Content
```Java
{
Name = amazon-route53-json-dns-request-success-dnsquery
 Vendor = Amazon
 Product = Amazon Route 53
 TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
 ParserVersion = v1.0.0
 Conditions = [""""rcode":""", """"srcids":""",  """"query_name":""", """"query_timestamp":""", """"query_class":""" ]
 Fields = [
   """"query_timestamp":"({time}\d\d\d\d\-\d\d\-\d\dT\d\d:\d\d:\d\dZ)"""
   """"srcaddr":"({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))"""
   """"query_name":"({dns_query}[^"]+)"""
   """"query_type":"({dns_query_type}[^"]+)"""
   """"rcode":"({dns_response_code}[^"]+)"""
   """"srcport":"({src_port}\d{1,5})"""
   """"query_class":"({dns_query_flags}[^"]+)"""
 ]


}
```