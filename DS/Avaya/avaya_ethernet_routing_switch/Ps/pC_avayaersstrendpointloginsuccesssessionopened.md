#### Parser Content
```Java
{
Name = "avaya-ers-str-endpoint-login-success-sessionopened"
Vendor = "Avaya"
Product = "Avaya Ethernet Routing Switch"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
"""Session opened"""
""" :#6"""
"""from IP address:"""
]
Fields = [
"""({event_name}Session opened)"""
"""IP address:\s+({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
]
ParserVersion = "v1.0.0"


}
```