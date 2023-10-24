#### Parser Content
```Java
{
Name = "splunk-stream-json-dns-response-success-messagetype"
Vendor = "Splunk"
Product = "Splunk Stream"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSS"
Conditions = [
""""reply_code":"""
""":dns""""
""""time_taken""""
""""message_type""""
]
Fields = [
  """"timestamp":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d{3})"""
  """"bytes":({bytes}\d+)"""
  """"dest_ip":"({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
  """"dest_mac":"({dest_mac}[a-fA-F\d:]+)"""
  """"dest_port":({dest_port}\d+)"""
  """"src_ip":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  """"src_mac":"({src_mac}[a-fA-F\d:]+)"""
  """"src_port":({src_port}\d+)"""
  """"time_taken":({time_taken}\d+)"""
  """"transport":"({protocol}[^"]+)"""
  """"ttl":\[({response_ttl}\d+)"""
  """"query":\["({dns_query}[^"]+)"""
  """"query_type":\["({dns_query_type}[^"]+)"""
  """"reply_code":"({dns_response_code}[^"]+)"""
  """"host_addr":\["({host}[^"]+)"""
  """"hostname":\["({host}[^"]+)"""
]
ParserVersion = "v1.0.0"


}
```