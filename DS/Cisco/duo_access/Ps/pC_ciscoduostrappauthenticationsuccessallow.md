#### Parser Content
```Java
{
Name = "cisco-duo-str-app-authentication-success-allow"
Vendor = "Cisco"
Product = "Duo Access"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
"""Duo authentication returned 'allow'"""
"""Success"""
]
Fields = [
"""({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)"""
"""\]\s+\(\(\'({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""\]\s+\(\(\'.+?\',\s*({session_id}\d+)\)"""
]
ParserVersion = "v1.0.0"


}
```