#### Parser Content
```Java
{
Name = "cisco-asa-str-endpoint-login-success-611101"
Vendor = "Cisco"
Product = "Cisco Adaptive Security Appliance"
TimeFormat = "MMM dd yyyy HH:mm:ss"
Conditions = [
"""-611101"""
"""%ASA-"""
]
Fields = [
"""%ASA\-({priority}\d+)\-({event_code}\d+)"""
"""({time}\w+ \d+ \d{4} \d\d:\d\d:\d\d):\s*%ASA"""
"""Uname:\s+(({email_address}[^@\s,]+@[^\.\s,"]+\.[^\s,"]+)|(({domain}[^\\\s,"]+)\\+)?({user}[^\s,"]+))"""
"""({event_name}User authentication succeeded)"""
"""IP address:\s*({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
]
DupFields = [
"host->dest_host"
]
ParserVersion = "v1.0.0"


}
```