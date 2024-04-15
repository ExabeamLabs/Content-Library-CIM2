#### Parser Content
```Java
{
Name = "cisco-asa-kv-endpoint-login-fail-113015"
Vendor = "Cisco"
Product = "Cisco Adaptive Security Appliance"
TimeFormat = "MMM dd yyyy HH:mm:ss"
Conditions = [
"""-113015"""
"""%ASA-"""
]
Fields = [
"""({time}\w+ \d\d \d\d\d\d \d\d:\d\d:\d\d)\s+({host}.+?)\s*:\s*%ASA-({priority}\d+)-({event_code}\d+)"""
"""({event_name}AAA user authentication Rejected)"""
"""\sreason\s*=\s*({failure_reason}.+?)\s*:"""
"""\suser\s*=\s*((\*+?)|({user}.+?))\s*:"""
"""\suser IP\s*=\s*({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
]
ParserVersion = "v1.0.0"


}
```