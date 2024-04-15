#### Parser Content
```Java
{
Name = "fireeye-networksecurity-json-http-session-dstdomain"
Vendor = "FireEye"
Product = "FireEye CMS"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
Conditions = [
""""uri_parsed": """"
""""useragent": """"
""""dstdomain": """"
]
Fields = [
""""eventtime":\s*"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)"""
""""uri_parsed":\s*"({uri_path}[^"]+)"""
""""srcipv4":\s*"({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
""""rcvdbodybytes":\s*({bytes_in}\d+)"""
""""sentbodybytes":\s*({bytes_out}\d+)"""
""""field":\s*"httpmethod/method"[^\}]*?"value":\s*"({method}[^"]+)"""
"""""value":\s*"({method}[^"]+)"[^\}]*?"field":\s*"httpmethod/method""""
""""dstipv4":\s*"({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
""""statuscode":\s*({http_response_code}\d+)"""
""""dstport":\s*({dest_port}\d+)"""
""""srcport":\s*({src_port}\d+)"""
""""rawmsghostname":\s*"({host}[^"]+)"""
""""dstdomain":\s*"({web_domain}[^"]+)"""
""""useragent":\s*"({user_agent}[^"]+)"""
]
ParserVersion = "v1.0.0"


}
```