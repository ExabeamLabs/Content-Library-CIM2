#### Parser Content
```Java
{
Name = "avaya-ers-str-app-authentication-fail-6"
Vendor = "Avaya"
Product = "Avaya Ethernet Routing Switch"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
"""Failed login"""
""" :#6"""
"""IP address:"""
]
Fields = [
"""({event_name}Failed login)"""
"""IP address:\s+({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
]
ParserVersion = "v1.0.0"


}
```