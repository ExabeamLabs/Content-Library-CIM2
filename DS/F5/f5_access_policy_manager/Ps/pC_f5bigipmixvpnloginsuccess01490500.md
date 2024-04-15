#### Parser Content
```Java
{
Name = "f5-bigip-mix-vpn-login-success-01490500"
Vendor = "F5"
Product = "F5 Access Policy Manager"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
"""01490500:5:"""
]
Fields = [
"""\d\d:\d\d\s+({host}[^\s]+)\s([^\s]+\s)?[^\s]+\[\d+\]"""
""""host":\{"name":"({host}[^"]+)"""
"""hostname="({host}[^"]+)"""
"""\s+01490500:5:.*?({session_id}[^\s:]+): New session"""
"""client IP ({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
]
ParserVersion = "v1.0.0"


}
```