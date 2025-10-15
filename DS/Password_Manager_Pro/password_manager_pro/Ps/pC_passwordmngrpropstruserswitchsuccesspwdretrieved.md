#### Parser Content
```Java
{
Name = "passwordmngrpro-p-str-user-switch-success-pwdretrieved"
Vendor = "Password Manager Pro"
Product = "Password Manager Pro"
TimeFormat = "yyyy/MM/dd HH:mm:ss"
Conditions = [
""" Password_Retrieved """
""" Success """
]
Fields = [
"""\s+(ResourceAudit:)?(({first_name}[^\s:_]+)(_({last_name}[^:\s]+))?):(?:({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?|({src_host}[^\s]+))\s+Password_Retrieved"""
"""({time}\d\d\d\d\/\d\d\/\d\d \d\d:\d\d:\d\d)"""
"""\w+ \d+ \d\d:\d\d:\d\d\s+({host}[^\s]+)"""
"""\w+ \d+ \d\d:\d\d:\d\d\s+({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
"""\sSuccess\s[^\s]+\s+({safe_value}[^:]+):({account}({dest_user}[^:]+)):"""
"""\s+(ResourceAudit:)?({user}[\w\.\-\!\#\^\~]{1,40}\$?):(?:(\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}))"""
]
ParserVersion = "v1.0.0"


}
```