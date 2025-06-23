#### Parser Content
```Java
{
Name = "cyberark-pam-cef-app-activity-success-catchall"
Vendor = "CyberArk"
Product = "CyberArk Privilege Access Manager"
TimeFormat = ["yyyy-MM-dd HH:mm:ss"]
Conditions = [
"""CEF:"""
"""|Cyber-Ark|Vault|"""
"""ProductName ="""
"""Cyber-Ark Vault"""
]
Fields = [
"""EventId=({event_code}\d+)"""
"""({app}Cyber-Ark)"""
"""EventMessage="*({operation}[^"=]+)"*\s\w+="""
"""EventSeverity=({severity}\d+)"""
"""ActingAddress=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))"""
"""ActionSourceUser=({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""
]
ParserVersion = "v1.0.0"


}
```