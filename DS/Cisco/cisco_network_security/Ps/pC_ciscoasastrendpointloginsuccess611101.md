#### Parser Content
```Java
{
Name = "cisco-asa-str-endpoint-login-success-611101"
Vendor = "Cisco"
Product = Cisco Network Security
TimeFormat = "MMM dd yyyy HH:mm:ss"
Conditions = [
"""-611101"""
"""%ASA-"""
]
Fields = [
"""%ASA\-({priority}\d+)\-({event_code}\d+)"""
"""({time}\w+ \d+ \d{4} \d\d:\d\d:\d\d).*?%ASA"""
"""Uname:\s+(({email_address}[^@\s,]+@[^\.\s,"]+\.[^\s,"]+)|(({domain}[^\\\s,"]+)\\+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""
"""({event_name}User authentication succeeded)"""
"""IP address:\s*({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""\s(::ffff:)?(-|({host}[\w\.-]+))[\s:]+%ASA-"""
]
DupFields = [
"host->dest_host"
]
ParserVersion = "v1.0.0"


}
```