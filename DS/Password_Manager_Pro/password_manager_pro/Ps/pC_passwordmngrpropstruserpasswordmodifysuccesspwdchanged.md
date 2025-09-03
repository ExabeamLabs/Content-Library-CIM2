#### Parser Content
```Java
{
Name = "passwordmngrpro-p-str-user-password-modify-success-pwdchanged"
Vendor = "Password Manager Pro"
Product = "Password Manager Pro"
TimeFormat = "yyyy/MM/dd HH:mm:ss"
Conditions = [
""" Password_Changed """
""" Success """
]
Fields = [
"""\s+(ResourceAudit:)?((System|({first_name}[^\s:_]+))(_({last_name}[^:\s]+))?):(?:({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?|({src_host}[^\s]+))\s+Password_Changed"""
"""\s+(ResourceAudit:)?({user}[\w\.\-\!\#\^\~]{1,40}\$?):(?:({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?|({src_host}[^\s]+))\s+Password_Changed"""
"""({time}\d\d\d\d\/\d\d\/\d\d \d\d:\d\d:\d\d)"""
"""\w+ \d+ \d\d:\d\d:\d\d\s+({host}[^\s]+)"""
"""\sSuccess\s[^\s]+\s+({safe_value}[^:]+):({dest_user}[^:]+):"""
]
ParserVersion = "v1.0.0"


}
```